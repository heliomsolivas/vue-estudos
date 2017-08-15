Num componente Vue temos de ter as coisas organizadas, para isso existem alguns conceitos/parametros a ter em conta e que são a maneira de funcionar de um componente.
# METHODS
Aqui deves guardar funções. Todo o tipo de funções que tratam dados e funcionalidade do componente.
Guardando essas funções no methods permite que eles sejam usados noutros componentes, por herança ou por grau de parentesco.
Aqui podes também importar métodos da store.
# DATA
Aqui deves guardas primitivos. Strings, arrays, objectos, etc. No fundo o estado do componente.
# COMPUTED

Aqui tens uma mistura dos dois anteriores, e entra a lógica/metodologia de programação reactiva. Estes métodos são funções que retornam dados são provaveis de terem sido alterados entre renderizações.
Num componente Vue temos de ter as coisas organizadas, para isso existem alguns conceitos/parametros a ter em conta e que são a maneira de funcionar de um componente.
Outra funcionalidade muito util é podermos importar da store os getters que vão para computed e os métodos da store que vão para os methods do componente.

# PROPS
Os dados passados ao componente. Esta é uma das poucas vias de passagem de dados, e permite controlos rígidos de tipagem. O que está no data é interno ao componente e possivelmente aos seus descendentes. O que está no props são dados para usar no componente e não podem ser mudados diretamente, só via mudança no estado do componente ou parte da aplicação que gera esses dados.

# WATCH
Aqui deves guardar métodos que devem ser chamados quando o valor de uma propriedade de data ou props mudar. Pode haver casos em que funcione usar computed, outras watch. Em regra geral, se houver algo que precises saber quando mudou usa watch; quando quiseres ter sempre dados atualizados, usa computed.