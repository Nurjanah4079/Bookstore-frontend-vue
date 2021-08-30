<template>
        <div id="katalogBuku">
            <h1 class="text-center">Katalog Buku</h1>
            <hr />
            <table class="table table-hover table-bordered">
                <thead>
                    <tr>
                        <th>No.</th>
                        <th>Judul</th>
                        <th>Pengarang</th>
                        <th>Harga</th>
                        <th>Stok</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(book, index) in bookList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ book.judul }}</td>
                        <td>{{ book.pengarang }}</td>
                        <td>{{ book.harga }}</td>
                        <td>{{ book.stok }}</td>
                        <!-- <td>
                            <button class="btn btn-info mr-3" @click="showEdit(book, index)">Edit</button>
                            <button class="btn btn-danger" @click="deleteBook(book, index)">Hapus</button>
                        </td> -->
                    </tr>
                </tbody>
            </table>
        </div>
</template>

<script>
export default {
    props: ["bookList"],
};
</script>

<style>
    h1 {
        text-align: center;
    }
</style>