<template>
  <b-navbar>
    <template slot="brand">
    </template>
    <template slot="start">
      <b-navbar-item to="/" tag="router-link">
        Inicio
      </b-navbar-item>
      <b-navbar-item to="/celula" tag="router-link">
        La Célula
      </b-navbar-item>
      <b-navbar-item to="/clasificacion" tag="router-link">
        Clasificación
      </b-navbar-item>
      <b-navbar-item to="/tipos" tag="router-link">
        Tipos
      </b-navbar-item>
      <b-navbar-item to="/tira" tag="router-link">
        Tira Cómica
      </b-navbar-item>
      <b-navbar-item to="/linea" tag="router-link">
        Línea de Tiempo
      </b-navbar-item>
      <b-navbar-item to="/actividades" tag="router-link">
        Actividades
      </b-navbar-item>
    </template>

    <template slot="end"> </template>
  </b-navbar>
</template>
