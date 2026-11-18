
# ProjetoSoftware-UMC

package com.valeviva.financeiro.model;

import jakarta.persistence.*;

import java.math.BigDecimal;

@Entity
@Table(name = "saldo_estoque")
public class SaldoEstoque {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "produto_id", nullable = false)
    private Long produtoId;

    @Column(name = "lote_codigo", nullable = false)
    private String loteCodigo;

    @Column(nullable = false, precision = 15, scale = 3)
    private BigDecimal quantidade;

    @Version
    private Long versao;
}