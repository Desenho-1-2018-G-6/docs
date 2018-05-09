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
as motivações do dono da aplicação. Sendo assim, é necessário que, dinamicamente, esse usuário adquira o status de administrador,
 herdando assim os atributos e métodos relacionados ao mesmo.
 #falar sobre outras possíveis escolhas

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

#todo
