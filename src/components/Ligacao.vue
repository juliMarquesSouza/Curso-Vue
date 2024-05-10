<template>
    <div>
        <div>
            One-way data binding <br>
            Two-way data binding <br>
            v-model -> formulários
        </div>

        <br><br>

        
        <div>
            <label>Nome</label> <br>
            <input
                v-model="name"
                type="text"
            > <br>
            {{ name }}
        </div>  
        <br><br>

        <div>
            <label>Sports</label> <br>
            <select v-model="sports">
                <option value="">Escolha</option>
                <option value="Futebol">Futebol</option>
                <option value="Skate">Skate</option>
                <option value="Tenis">Tenis</option>
            </select> <br>
            {{ sports }}
        </div> 

            <br><br>

        <div>
            <label>Newsletter</label> <br>
            <input 
                v-model="newsletter"
                type="radio"
                value="Sim"
            >Sim 
            <input 
                v-model="newsletter"
                type="radio"
                value="Não"
            >Não <br>
            {{ newsletter }}
        </div>

        <br><br>

        <div>
            <label>Contrato</label> <br>
            <input 
                v-model="contract"
                type="checkbox"
            > Aceita nossos termos... <br>

                {{ contract }}


        </div>
    </div>
</template>

<script>

export default {
    name: 'Ligacao',
    data() {
        return {
            name: 'jon snow',
            sports: '',
            newsletter: '',
            contract: false,
        }
    }        
}
</script>




