# Calculo-idade-simples

import React, {useState} from 'react';
import { StyleSheet, Text, View, Image, TextInput, TouchableOpacity } from 'react-native';


export default function App() {

const [anoAtual, setAnoatual] = useState ('');
const [anoNasc, setAnonasc] = useState ('');

function CalcularIdade(){

  const Idade = parseInt(anoAtual) - parseInt(anoNasc);

  alert ("Você têm ou terá " +Idade+ " anos de idade nesse ano! Tá velho em");


}
  return (
    <View style={styles.container}>

      <Text style={styles.titulo}>Qual a minha Idade ?</Text>

      <TextInput style={styles.campo} placeholder="Digite o ano atual:"
      keyboardType='numeric' onChangeText={setAnoatual}>
      </TextInput>



      <TextInput style={styles.campo} placeholder="Digite o ano em que você nasceu:"
      keyboardType='numeric' onChangeText={setAnonasc}>
      </TextInput>  

      <TouchableOpacity style={styles.botao} onPress ={CalcularIdade}>
        <Text style={styles.textoBotao}>
        Calcular Idade
        </Text>
      </TouchableOpacity>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
  flex: 1,
  backgroundColor: '#fff',
},


titulo:{
  textAlign: 'center',
    marginTop: 40,
    marginBottom: 40,
    fontSize: 30,
    color:"#000",
},

campo:{
  backgroundColor: '#fff',
  borderRadius: 30,
  margin: 15,
  padding: 10,
  fontSize: 15,
},



botao:{
    justifyContent: 'center',
    alignItems: 'center',
    margin:15,
    backgroundColor:'#FFD700',
    padding: 10,
},

textoBotao:{
  fontSize: '40',
  
},

});
