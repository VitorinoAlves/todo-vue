<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp']);
</script>

<template>
    <form action="" class="row" @submit.prevent="props.cadastraTarefa">
        <div class="col">
            <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" type="text" placeholder="Digite aqui a descrição da tarefa" class="form-control" required>
        </div>
        <div class="col-md-2">
            <button type="submit" class="btn btn-primary">Cadastrar</button>
        </div>
        <div class="col-md-2">
            <select @change="props.trocarFiltro" class="form-control">
                <option value="todas">Todas as tarefas</option>
                <option value="pendentes">Pendentes</option>
                <option value="finalizadas">Finalizadas</option>
            </select>
        </div>
    </form>
</template>