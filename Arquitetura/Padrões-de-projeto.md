|    Data    | Versão | Modificação | Autor |
|:----------:|:------:|:--:|:---------------:|
| 09/05/2018 | 1.0 | Inicialização do documento | Lucas Malta |
------------------------------------

# Padrões de projeto

Este documento tem como objetivo explicitar os padrões de projeto utilizados nesta aplicação
nos níveis de modelagem e de implementação, bem como a motivação para o uso dos mesmos.

## 1- Decorator
O padrão de projeto decorator visa anexar responsabilidades adicionais a um objeto de modo dinâmico. Desse modo, um objeto
pode ter novos atributos e/ou métodos sem a necessidade de deletá-lo/recriá-lo.

Esse padrão foi introduzido em nossa aplicação no contexto de Usuário - Administrador. Um usuário, ao ser criado, contém os
atributos e métodos somente de um usuário comum. Contudo, esse mesmo usuário pode adquirir o status de um administrador, dada
as motivações do dono da aplicação. Sendo assim, é necessário que, dinamicamente, esse usuário adquira o status de administrador, herdando assim os atributos e métodos relacionados ao mesmo. Outros padrões poderiam ser aplicados, como o facade ou até mesmo um padrão de criação como o builder, mas achamos a ideia do Decorator mais interessante, pela possibilidade de adicionar/remover métodos e atributos dinamicamente à um objeto.


Dada as limitações do framework/linguagem, a aplicação do padrão decorator teve algumas mudanças para que o mesmo se adequa-se 
ao ambiente. A primeira limitação se refere à maneira que o decorator injeta novas "subclasses" à classe principal. Como a herança
do rails é limitada (Além de não se existir uma classe abstrata propriamente dita), tivemos que optar por utilizar um campo chamado 
"user_type". Esse campo (String), contém os tipos de decorators que estão sendo adicionados. Na aplicação atual, só temos um tipo
 de decorator, o admin. Mas caso houvesse mais, poderiamos adicionar ao user_type: "admin manager seller", que o usuário obteria
 os métodos e atributos de manager e seller.

```Ruby
  create_table "users", force: :cascade do |t|
    t.string   "first_name"
    t.string   "last_name"
    t.string   "email"
    t.string   "cpf"
    t.date     "birth_date"
    t.string   "gender"
    t.string   "phone"
    t.datetime "created_at",      null: false
    t.datetime "updated_at",      null: false
    t.string   "password_digest"
    t.string   "user_type"
  end
```
Adicionado o tipo de usuário no campo, o mesmo "herda" os métodos e atributos da classe definida. Desse modo, definimos:
```Ruby
class UserDecorator < Draper::Decorator
  include Draper::LazyHelpers
  delegate_all

  def show_sidebar
    if current_user.user_type.include? "admin"
      render :partial => "users/admin_sidebar"
    end
  end

  def show_edit_buttons
    if current_user.user_type.include? "admin"
      return true
    else
      return false
    end
  end

```
Esses 2 métodos são para usuários que foram decorados com a classe de Admin. Esses usuários podem utilizar os métodos show_sidebar e show_edit_buttons, que são métodos que liberam o uso de outras funcionalidades específicas para administrador, como adição/remoção de produtos.
