project('z3', 'cpp', version: '3049f578a8f98a0b0992eca193afe57a73b30ca3')

python = import('python').find_installation()

# Run Z3's configuration script
run_command(python, 'scripts/mk_make.py', check: true)

z3_src = [
    'src/ackermannization/lackr.cpp',
    'src/ackermannization/ackr_bound_probe.cpp',
    'src/ackermannization/ackermannize_bv_tactic.cpp',
    'src/ackermannization/ackr_helper.cpp',
    'src/ackermannization/ackr_model_converter.cpp',
    'src/ackermannization/ackr_bound_probe.cpp',
    'src/ackermannization/ackermannize_bv_tactic.cpp',
    'src/ackermannization/ackermannize_bv_model_converter.cpp',
    'src/ackermannization/lackr_model_constructor.cpp',
    'src/api/api_algebraic.cpp',
    'src/api/api_arith.cpp',
    'src/api/api_array.cpp',
    'src/api/api_ast.cpp',
    'src/api/dll/gparams_register_modules.cpp',
    'src/api/api_ast_map.cpp',
    'src/api/api_ast_vector.cpp',
    'src/api/api_bv.cpp',
    'src/api/api_config_params.cpp',
    'src/api/api_context.cpp',
    'src/api/api_datalog.cpp',
    'src/api/api_datatype.cpp',
    'src/api/api_fpa.cpp',
    'src/api/api_goal.cpp',
    'src/api/api_log.cpp',
    'src/api/api_commands.cpp',
    'src/api/api_log_macros.cpp',
    'src/api/api_model.cpp',
    'src/api/api_numeral.cpp',
    'src/api/api_opt.cpp',
    'src/api/api_params.cpp',
    'src/api/api_parsers.cpp',
    'src/api/api_pb.cpp',
    'src/api/api_polynomial.cpp',
    'src/api/api_qe.cpp',
    'src/api/api_quant.cpp',
    'src/api/api_rcf.cpp',
    'src/api/api_seq.cpp',
    'src/api/api_solver.cpp',
    'src/tactic/smtlogics/quant_tactics.cpp',
    'src/api/api_special_relations.cpp',
    'src/api/api_stats.cpp',
    'src/api/api_tactic.cpp',
    'src/api/z3_replayer.cpp',
    'src/ast/act_cache.cpp',
    'src/ast/arith_decl_plugin.cpp',
    'src/ast/array_decl_plugin.cpp',
    'src/ast/array_peq.cpp',
    'src/ast/ast.cpp',
    'src/ast/ast_ll_pp.cpp',
    'src/ast/ast_lt.cpp',
    'src/ast/ast_pp_dot.cpp',
    'src/ast/ast_pp_util.cpp',
    'src/ast/ast_printer.cpp',
    'src/ast/ast_smt2_pp.cpp',
    'src/ast/ast_smt_pp.cpp',
    'src/ast/ast_translation.cpp',
    'src/ast/ast_util.cpp',
    'src/ast/bv_decl_plugin.cpp',
    'src/ast/char_decl_plugin.cpp',
    'src/ast/converters/equiv_proof_converter.cpp',
    'src/ast/converters/expr_inverter.cpp',
    'src/ast/converters/generic_model_converter.cpp',
    'src/ast/converters/horn_subsume_model_converter.cpp',
    'src/ast/converters/model_converter.cpp',
    'src/ast/converters/proof_converter.cpp',
    'src/ast/converters/replace_proof_converter.cpp',
    'src/ast/cost_evaluator.cpp',
    'src/ast/datatype_decl_plugin.cpp',
    'src/ast/decl_collector.cpp',
    'src/ast/display_dimacs.cpp',
    'src/ast/dl_decl_plugin.cpp',
    'src/ast/euf/euf_ac_plugin.cpp',
    'src/ast/euf/euf_arith_plugin.cpp',
    'src/ast/euf/euf_bv_plugin.cpp',
    'src/ast/euf/euf_egraph.cpp',
    'src/ast/euf/euf_enode.cpp',
    'src/ast/euf/euf_etable.cpp',
    'src/ast/euf/euf_justification.cpp',
    'src/ast/euf/euf_plugin.cpp',
    'src/ast/euf/euf_specrel_plugin.cpp',
    'src/ast/expr2polynomial.cpp',
    'src/ast/expr2var.cpp',
    'src/ast/expr_abstract.cpp',
    'src/ast/expr_functors.cpp',
    'src/ast/expr_map.cpp',
    'src/ast/expr_stat.cpp',
    'src/ast/expr_substitution.cpp',
    'src/ast/for_each_ast.cpp',
    'src/ast/for_each_expr.cpp',
    'src/ast/format.cpp',
    'src/ast/fpa/bv2fpa_converter.cpp',
    'src/ast/fpa/fpa2bv_converter.cpp',
    'src/ast/fpa/fpa2bv_rewriter.cpp',
    'src/ast/fpa_decl_plugin.cpp',
    'src/ast/func_decl_dependencies.cpp',
    'src/ast/has_free_vars.cpp',
    'src/ast/macro_substitution.cpp',
    'src/ast/macros/macro_finder.cpp',
    'src/ast/macros/macro_manager.cpp',
    'src/ast/macros/macro_util.cpp',
    'src/ast/macros/quantifier_macro_info.cpp',
    'src/ast/macros/quasi_macros.cpp',
    'src/ast/normal_forms/defined_names.cpp',
    'src/ast/normal_forms/elim_term_ite.cpp',
    'src/ast/normal_forms/name_exprs.cpp',
    'src/ast/normal_forms/nnf.cpp',
    'src/ast/normal_forms/pull_quant.cpp',
    'src/ast/num_occurs.cpp',
    'src/ast/occurs.cpp',
    'src/ast/pattern/expr_pattern_match.cpp',
    'src/ast/pattern/pattern_inference.cpp',
    'src/ast/pb_decl_plugin.cpp',
    'src/ast/polymorphism_inst.cpp',
    'src/ast/polymorphism_util.cpp',
    'src/ast/pp.cpp',
    'src/ast/proofs/proof_checker.cpp',
    'src/ast/proofs/proof_utils.cpp',
    'src/ast/quantifier_stat.cpp',
    'src/ast/recfun_decl_plugin.cpp',
    'src/ast/reg_decl_plugins.cpp',
    'src/ast/rewriter/arith_rewriter.cpp',
    'src/ast/rewriter/array_rewriter.cpp',
    'src/ast/rewriter/ast_counter.cpp',
    'src/ast/rewriter/bit2int.cpp',
    'src/ast/rewriter/bit_blaster/bit_blaster.cpp',
    'src/ast/rewriter/bit_blaster/bit_blaster_rewriter.cpp',
    'src/ast/rewriter/bool_rewriter.cpp',
    'src/ast/rewriter/bv_bounds.cpp',
    'src/ast/rewriter/bv_elim.cpp',
    'src/ast/rewriter/bv_rewriter.cpp',
    'src/ast/rewriter/cached_var_subst.cpp',
    'src/ast/rewriter/char_rewriter.cpp',
    'src/ast/rewriter/datatype_rewriter.cpp',
    'src/ast/rewriter/der.cpp',
    'src/ast/rewriter/distribute_forall.cpp',
    'src/ast/rewriter/dl_rewriter.cpp',
    'src/ast/rewriter/dom_simplifier.cpp',
    'src/ast/rewriter/elim_bounds.cpp',
    'src/ast/rewriter/enum2bv_rewriter.cpp',
    'src/ast/rewriter/expr_replacer.cpp',
    'src/ast/rewriter/expr_safe_replace.cpp',
    'src/ast/rewriter/factor_equivs.cpp',
    'src/ast/rewriter/factor_rewriter.cpp',
    'src/ast/rewriter/fpa_rewriter.cpp',
    'src/ast/rewriter/func_decl_replace.cpp',
    'src/ast/rewriter/inj_axiom.cpp',
    'src/ast/rewriter/label_rewriter.cpp',
    'src/ast/rewriter/macro_replacer.cpp',
    'src/ast/rewriter/maximize_ac_sharing.cpp',
    'src/ast/rewriter/mk_extract_proc.cpp',
    'src/ast/rewriter/mk_simplified_app.cpp',
    'src/ast/rewriter/pb2bv_rewriter.cpp',
    'src/ast/rewriter/pb_rewriter.cpp',
    'src/ast/rewriter/push_app_ite.cpp',
    'src/ast/rewriter/quant_hoist.cpp',
    'src/ast/rewriter/recfun_rewriter.cpp',
    'src/ast/rewriter/rewriter.cpp',
    'src/ast/rewriter/seq_axioms.cpp',
    'src/ast/rewriter/seq_eq_solver.cpp',
    'src/ast/rewriter/seq_rewriter.cpp',
    'src/ast/rewriter/seq_skolem.cpp',
    'src/ast/rewriter/th_rewriter.cpp',
    'src/ast/rewriter/value_sweep.cpp',
    'src/ast/rewriter/var_subst.cpp',
    'src/ast/seq_decl_plugin.cpp',
    'src/ast/shared_occs.cpp',
    'src/ast/simplifiers/bit_blaster.cpp',
    'src/ast/simplifiers/bound_manager.cpp',
    'src/ast/simplifiers/bound_propagator.cpp',
    'src/ast/simplifiers/bound_simplifier.cpp',
    'src/ast/simplifiers/bv_bounds_simplifier.cpp',
    'src/ast/simplifiers/bv_slice.cpp',
    'src/ast/simplifiers/card2bv.cpp',
    'src/ast/simplifiers/demodulator_simplifier.cpp',
    'src/ast/simplifiers/dependent_expr_state.cpp',
    'src/ast/simplifiers/distribute_forall.cpp',
    'src/ast/simplifiers/dominator_simplifier.cpp',
    'src/ast/simplifiers/elim_unconstrained.cpp',
    'src/ast/simplifiers/eliminate_predicates.cpp',
    'src/ast/simplifiers/euf_completion.cpp',
    'src/ast/simplifiers/extract_eqs.cpp',
    'src/ast/simplifiers/linear_equation.cpp',
    'src/ast/simplifiers/max_bv_sharing.cpp',
    'src/ast/simplifiers/model_reconstruction_trail.cpp',
    'src/ast/simplifiers/propagate_values.cpp',
    'src/ast/simplifiers/reduce_args_simplifier.cpp',
    'src/ast/simplifiers/solve_context_eqs.cpp',
    'src/ast/simplifiers/solve_eqs.cpp',
    'src/ast/sls/bv_sls.cpp',
    'src/ast/sls/bv_sls_eval.cpp',
    'src/ast/sls/bv_sls_fixed.cpp',
    'src/ast/sls/bv_sls_terms.cpp',
    'src/ast/sls/bvsls_opt_engine.cpp',
    'src/ast/sls/sls_engine.cpp',
    'src/ast/sls/sls_valuation.cpp',
    'src/ast/special_relations_decl_plugin.cpp',
    'src/ast/static_features.cpp',
    'src/ast/substitution/demodulator_rewriter.cpp',
    'src/ast/substitution/matcher.cpp',
    'src/ast/substitution/substitution.cpp',
    'src/ast/substitution/substitution_tree.cpp',
    'src/ast/substitution/unifier.cpp',
    'src/ast/used_vars.cpp',
    'src/ast/value_generator.cpp',
    'src/ast/well_sorted.cpp',
    'src/cmd_context/basic_cmds.cpp',
    'src/cmd_context/cmd_context.cpp',
    'src/cmd_context/cmd_context_to_goal.cpp',
    'src/cmd_context/cmd_util.cpp',
    'src/cmd_context/echo_tactic.cpp',
    'src/cmd_context/eval_cmd.cpp',
    'src/cmd_context/extra_cmds/dbg_cmds.cpp',
    'src/cmd_context/extra_cmds/polynomial_cmds.cpp',
    'src/cmd_context/extra_cmds/proof_cmds.cpp',
    'src/cmd_context/extra_cmds/subpaving_cmds.cpp',
    'src/cmd_context/parametric_cmd.cpp',
    'src/cmd_context/pdecl.cpp',
    'src/cmd_context/simplifier_cmds.cpp',
    'src/cmd_context/simplify_cmd.cpp',
    'src/cmd_context/tactic_cmds.cpp',
    'src/cmd_context/tactic_manager.cpp',
    'src/math/automata/automaton.cpp',
    'src/math/dd/dd_bdd.cpp',
    'src/math/dd/dd_fdd.cpp',
    'src/math/dd/dd_pdd.cpp',
    'src/math/grobner/grobner.cpp',
    'src/math/grobner/pdd_simplifier.cpp',
    'src/math/grobner/pdd_solver.cpp',
    'src/math/hilbert/hilbert_basis.cpp',
    'src/math/interval/dep_intervals.cpp',
    'src/math/interval/interval_mpq.cpp',
    'src/math/lp/core_solver_pretty_printer.cpp',
    'src/math/lp/dense_matrix.cpp',
    'src/math/lp/emonics.cpp',
    'src/math/lp/factorization.cpp',
    'src/math/lp/factorization_factory_imp.cpp',
    'src/math/lp/gomory.cpp',
    'src/math/lp/hnf_cutter.cpp',
    'src/math/lp/horner.cpp',
    'src/math/lp/indexed_vector.cpp',
    'src/math/lp/int_branch.cpp',
    'src/math/lp/int_cube.cpp',
    'src/math/lp/int_gcd_test.cpp',
    'src/math/lp/int_solver.cpp',
    'src/math/lp/lar_core_solver.cpp',
    'src/math/lp/lar_solver.cpp',
    'src/math/lp/lp_core_solver_base.cpp',
    'src/math/lp/lp_primal_core_solver.cpp',
    'src/math/lp/lp_settings.cpp',
    'src/math/lp/matrix.cpp',
    'src/math/lp/mon_eq.cpp',
    'src/math/lp/monomial_bounds.cpp',
    'src/math/lp/nex_creator.cpp',
    'src/math/lp/nla_basics_lemmas.cpp',
    'src/math/lp/nla_common.cpp',
    'src/math/lp/nla_core.cpp',
    'src/math/lp/nla_divisions.cpp',
    'src/math/lp/nla_grobner.cpp',
    'src/math/lp/nla_intervals.cpp',
    'src/math/lp/nla_monotone_lemmas.cpp',
    'src/math/lp/nla_order_lemmas.cpp',
    'src/math/lp/nla_powers.cpp',
    'src/math/lp/nla_solver.cpp',
    'src/math/lp/nla_tangent_lemmas.cpp',
    'src/math/lp/nra_solver.cpp',
    'src/math/lp/permutation_matrix.cpp',
    'src/math/lp/random_updater.cpp',
    'src/math/lp/static_matrix.cpp',
    'src/math/polynomial/algebraic_numbers.cpp',
    'src/math/polynomial/polynomial.cpp',
    'src/math/polynomial/polynomial_cache.cpp',
    'src/math/polynomial/rpolynomial.cpp',
    'src/math/polynomial/sexpr2upolynomial.cpp',
    'src/math/polynomial/upolynomial.cpp',
    'src/math/polynomial/upolynomial_factorization.cpp',
    'src/math/realclosure/mpz_matrix.cpp',
    'src/math/realclosure/realclosure.cpp',
    'src/math/simplex/bit_matrix.cpp',
    'src/math/simplex/model_based_opt.cpp',
    'src/math/simplex/simplex.cpp',
    'src/math/subpaving/subpaving.cpp',
    'src/math/subpaving/subpaving_hwf.cpp',
    'src/math/subpaving/subpaving_mpf.cpp',
    'src/math/subpaving/subpaving_mpff.cpp',
    'src/math/subpaving/subpaving_mpfx.cpp',
    'src/math/subpaving/subpaving_mpq.cpp',
    'src/math/subpaving/tactic/expr2subpaving.cpp',
    'src/math/subpaving/tactic/subpaving_tactic.cpp',
    'src/model/array_factory.cpp',
    'src/model/datatype_factory.cpp',
    'src/model/func_interp.cpp',
    'src/model/model.cpp',
    'src/model/model2expr.cpp',
    'src/model/model_core.cpp',
    'src/model/model_evaluator.cpp',
    'src/model/model_implicant.cpp',
    'src/model/model_macro_solver.cpp',
    'src/model/model_pp.cpp',
    'src/model/model_smt2_pp.cpp',
    'src/model/model_v2_pp.cpp',
    'src/model/numeral_factory.cpp',
    'src/model/struct_factory.cpp',
    'src/model/value_factory.cpp',
    'src/muz/base/bind_variables.cpp',
    'src/muz/base/dl_boogie_proof.cpp',
    'src/muz/base/dl_context.cpp',
    'src/muz/base/dl_costs.cpp',
    'src/muz/base/dl_rule.cpp',
    'src/muz/base/dl_rule_set.cpp',
    'src/muz/base/dl_rule_subsumption_index.cpp',
    'src/muz/base/dl_rule_transformer.cpp',
    'src/muz/base/dl_util.cpp',
    'src/muz/base/hnf.cpp',
    'src/muz/base/rule_properties.cpp',
    'src/muz/bmc/dl_bmc_engine.cpp',
    'src/muz/clp/clp_context.cpp',
    'src/muz/dataflow/dataflow.cpp',
    'src/muz/ddnf/ddnf.cpp',
    'src/muz/fp/datalog_parser.cpp',
    'src/muz/fp/dl_cmds.cpp',
    'src/muz/fp/dl_register_engine.cpp',
    'src/muz/fp/horn_tactic.cpp',
    'src/muz/rel/aig_exporter.cpp',
    'src/muz/rel/check_relation.cpp',
    'src/muz/rel/dl_base.cpp',
    'src/muz/rel/dl_bound_relation.cpp',
    'src/muz/rel/dl_check_table.cpp',
    'src/muz/rel/dl_compiler.cpp',
    'src/muz/rel/dl_external_relation.cpp',
    'src/muz/rel/dl_finite_product_relation.cpp',
    'src/muz/rel/dl_instruction.cpp',
    'src/muz/rel/dl_interval_relation.cpp',
    'src/muz/rel/dl_lazy_table.cpp',
    'src/muz/rel/dl_mk_explanations.cpp',
    'src/muz/rel/dl_mk_similarity_compressor.cpp',
    'src/muz/rel/dl_mk_simple_joins.cpp',
    'src/muz/rel/dl_product_relation.cpp',
    'src/muz/rel/dl_relation_manager.cpp',
    'src/muz/rel/dl_sieve_relation.cpp',
    'src/muz/rel/dl_sparse_table.cpp',
    'src/muz/rel/dl_table.cpp',
    'src/muz/rel/dl_table_relation.cpp',
    'src/muz/rel/doc.cpp',
    'src/muz/rel/karr_relation.cpp',
    'src/muz/rel/rel_context.cpp',
    'src/muz/rel/udoc_relation.cpp',
    'src/muz/spacer/spacer_antiunify.cpp',
    'src/muz/spacer/spacer_arith_generalizers.cpp',
    'src/muz/spacer/spacer_arith_kernel.cpp',
    'src/muz/spacer/spacer_callback.cpp',
    'src/muz/spacer/spacer_cluster.cpp',
    'src/muz/spacer/spacer_cluster_util.cpp',
    'src/muz/spacer/spacer_concretize.cpp',
    'src/muz/spacer/spacer_conjecture.cpp',
    'src/muz/spacer/spacer_context.cpp',
    'src/muz/spacer/spacer_convex_closure.cpp',
    'src/muz/spacer/spacer_dl_interface.cpp',
    'src/muz/spacer/spacer_expand_bnd_generalizer.cpp',
    'src/muz/spacer/spacer_farkas_learner.cpp',
    'src/muz/spacer/spacer_generalizers.cpp',
    'src/muz/spacer/spacer_global_generalizer.cpp',
    'src/muz/spacer/spacer_ind_lemma_generalizer.cpp',
    'src/muz/spacer/spacer_iuc_proof.cpp',
    'src/muz/spacer/spacer_iuc_solver.cpp',
    'src/muz/spacer/spacer_legacy_frames.cpp',
    'src/muz/spacer/spacer_legacy_mbp.cpp',
    'src/muz/spacer/spacer_legacy_mev.cpp',
    'src/muz/spacer/spacer_manager.cpp',
    'src/muz/spacer/spacer_matrix.cpp',
    'src/muz/spacer/spacer_mbc.cpp',
    'src/muz/spacer/spacer_mev_array.cpp',
    'src/muz/spacer/spacer_pdr.cpp',
    'src/muz/spacer/spacer_proof_utils.cpp',
    'src/muz/spacer/spacer_prop_solver.cpp',
    'src/muz/spacer/spacer_qe_project.cpp',
    'src/muz/spacer/spacer_quant_generalizer.cpp',
    'src/muz/spacer/spacer_sat_answer.cpp',
    'src/muz/spacer/spacer_sem_matcher.cpp',
    'src/muz/spacer/spacer_sym_mux.cpp',
    'src/muz/spacer/spacer_unsat_core_learner.cpp',
    'src/muz/spacer/spacer_unsat_core_plugin.cpp',
    'src/muz/spacer/spacer_util.cpp',
    'src/muz/tab/tab_context.cpp',
    'src/muz/transforms/dl_mk_array_blast.cpp',
    'src/muz/transforms/dl_mk_array_eq_rewrite.cpp',
    'src/muz/transforms/dl_mk_array_instantiation.cpp',
    'src/muz/transforms/dl_mk_backwards.cpp',
    'src/muz/transforms/dl_mk_bit_blast.cpp',
    'src/muz/transforms/dl_mk_coalesce.cpp',
    'src/muz/transforms/dl_mk_coi_filter.cpp',
    'src/muz/transforms/dl_mk_elim_term_ite.cpp',
    'src/muz/transforms/dl_mk_filter_rules.cpp',
    'src/muz/transforms/dl_mk_interp_tail_simplifier.cpp',
    'src/muz/transforms/dl_mk_karr_invariants.cpp',
    'src/muz/transforms/dl_mk_loop_counter.cpp',
    'src/muz/transforms/dl_mk_magic_sets.cpp',
    'src/muz/transforms/dl_mk_magic_symbolic.cpp',
    'src/muz/transforms/dl_mk_quantifier_abstraction.cpp',
    'src/muz/transforms/dl_mk_quantifier_instantiation.cpp',
    'src/muz/transforms/dl_mk_rule_inliner.cpp',
    'src/muz/transforms/dl_mk_scale.cpp',
    'src/muz/transforms/dl_mk_separate_negated_tails.cpp',
    'src/muz/transforms/dl_mk_slice.cpp',
    'src/muz/transforms/dl_mk_subsumption_checker.cpp',
    'src/muz/transforms/dl_mk_synchronize.cpp',
    'src/muz/transforms/dl_mk_unbound_compressor.cpp',
    'src/muz/transforms/dl_mk_unfold.cpp',
    'src/muz/transforms/dl_transforms.cpp',
    'src/nlsat/nlsat_clause.cpp',
    'src/nlsat/nlsat_evaluator.cpp',
    'src/nlsat/nlsat_explain.cpp',
    'src/nlsat/nlsat_interval_set.cpp',
    'src/nlsat/nlsat_solver.cpp',
    'src/nlsat/nlsat_types.cpp',
    'src/nlsat/tactic/goal2nlsat.cpp',
    'src/nlsat/tactic/nlsat_tactic.cpp',
    'src/nlsat/tactic/qfnra_nlsat_tactic.cpp',
    'src/opt/maxcore.cpp',
    'src/opt/maxlex.cpp',
    'src/opt/maxsmt.cpp',
    'src/opt/opt_cmds.cpp',
    'src/opt/opt_context.cpp',
    'src/opt/opt_cores.cpp',
    'src/opt/opt_lns.cpp',
    'src/opt/opt_pareto.cpp',
    'src/opt/opt_parse.cpp',
    'src/opt/opt_preprocess.cpp',
    'src/opt/opt_solver.cpp',
    'src/opt/optsmt.cpp',
    'src/opt/pb_sls.cpp',
    'src/opt/sortmax.cpp',
    'src/opt/totalizer.cpp',
    'src/opt/wmax.cpp',
    'src/params/context_params.cpp',
    'src/params/pattern_inference_params.cpp',
    'src/parsers/smt2/marshal.cpp',
    'src/parsers/smt2/smt2parser.cpp',
    'src/parsers/smt2/smt2scanner.cpp',
    'src/parsers/util/cost_parser.cpp',
    'src/parsers/util/pattern_validation.cpp',
    'src/parsers/util/scanner.cpp',
    'src/parsers/util/simple_parser.cpp',
    'src/qe/lite/qe_lite_tactic.cpp',
    'src/qe/lite/qel.cpp',
    'src/qe/mbp/mbp_arith.cpp',
    'src/qe/mbp/mbp_arrays.cpp',
    'src/qe/mbp/mbp_arrays_tg.cpp',
    'src/qe/mbp/mbp_basic_tg.cpp',
    'src/qe/mbp/mbp_datatypes.cpp',
    'src/qe/mbp/mbp_dt_tg.cpp',
    'src/qe/mbp/mbp_plugin.cpp',
    'src/qe/mbp/mbp_qel.cpp',
    'src/qe/mbp/mbp_qel_util.cpp',
    'src/qe/mbp/mbp_solve_plugin.cpp',
    'src/qe/mbp/mbp_term_graph.cpp',
    'src/qe/nlarith_util.cpp',
    'src/qe/nlqsat.cpp',
    'src/qe/qe.cpp',
    'src/qe/qe_arith_plugin.cpp',
    'src/qe/qe_array_plugin.cpp',
    'src/qe/qe_bool_plugin.cpp',
    'src/qe/qe_bv_plugin.cpp',
    'src/qe/qe_cmd.cpp',
    'src/qe/qe_datatype_plugin.cpp',
    'src/qe/qe_dl_plugin.cpp',
    'src/qe/qe_mbi.cpp',
    'src/qe/qe_mbp.cpp',
    'src/qe/qe_tactic.cpp',
    'src/qe/qsat.cpp',
    'src/sat/dimacs.cpp',
    'src/sat/sat_aig_cuts.cpp',
    'src/sat/sat_aig_finder.cpp',
    'src/sat/sat_anf_simplifier.cpp',
    'src/sat/sat_asymm_branch.cpp',
    'src/sat/sat_bcd.cpp',
    'src/sat/sat_big.cpp',
    'src/sat/sat_binspr.cpp',
    'src/sat/sat_clause.cpp',
    'src/sat/sat_clause_set.cpp',
    'src/sat/sat_clause_use_list.cpp',
    'src/sat/sat_cleaner.cpp',
    'src/sat/sat_config.cpp',
    'src/sat/sat_cut_simplifier.cpp',
    'src/sat/sat_cutset.cpp',
    'src/sat/sat_ddfw.cpp',
    'src/sat/sat_drat.cpp',
    'src/sat/sat_elim_eqs.cpp',
    'src/sat/sat_elim_vars.cpp',
    'src/sat/sat_gc.cpp',
    'src/sat/sat_integrity_checker.cpp',
    'src/sat/sat_local_search.cpp',
    'src/sat/sat_lookahead.cpp',
    'src/sat/sat_lut_finder.cpp',
    'src/sat/sat_model_converter.cpp',
    'src/sat/sat_mus.cpp',
    'src/sat/sat_npn3_finder.cpp',
    'src/sat/sat_parallel.cpp',
    'src/sat/sat_prob.cpp',
    'src/sat/sat_probing.cpp',
    'src/sat/sat_proof_trim.cpp',
    'src/sat/sat_scc.cpp',
    'src/sat/sat_simplifier.cpp',
    'src/sat/sat_solver.cpp',
    'src/sat/sat_solver/inc_sat_solver.cpp',
    'src/sat/sat_solver/sat_smt_solver.cpp',
    'src/sat/sat_watched.cpp',
    'src/sat/sat_xor_finder.cpp',
    'src/sat/smt/arith_axioms.cpp',
    'src/sat/smt/arith_diagnostics.cpp',
    'src/sat/smt/arith_internalize.cpp',
    'src/sat/smt/arith_sls.cpp',
    'src/sat/smt/arith_solver.cpp',
    'src/sat/smt/arith_value.cpp',
    'src/sat/smt/array_axioms.cpp',
    'src/sat/smt/array_diagnostics.cpp',
    'src/sat/smt/array_internalize.cpp',
    'src/sat/smt/array_model.cpp',
    'src/sat/smt/array_solver.cpp',
    'src/sat/smt/atom2bool_var.cpp',
    'src/sat/smt/bv_ackerman.cpp',
    'src/sat/smt/bv_delay_internalize.cpp',
    'src/sat/smt/bv_internalize.cpp',
    'src/sat/smt/bv_invariant.cpp',
    'src/sat/smt/bv_solver.cpp',
    'src/sat/smt/bv_theory_checker.cpp',
    'src/sat/smt/dt_solver.cpp',
    'src/sat/smt/euf_ackerman.cpp',
    'src/sat/smt/euf_internalize.cpp',
    'src/sat/smt/euf_invariant.cpp',
    'src/sat/smt/euf_local_search.cpp',
    'src/sat/smt/euf_model.cpp',
    'src/sat/smt/euf_proof.cpp',
    'src/sat/smt/euf_proof_checker.cpp',
    'src/sat/smt/euf_relevancy.cpp',
    'src/sat/smt/euf_solver.cpp',
    'src/sat/smt/fpa_solver.cpp',
    'src/sat/smt/intblast_solver.cpp',
    'src/sat/smt/pb_card.cpp',
    'src/sat/smt/pb_constraint.cpp',
    'src/sat/smt/pb_internalize.cpp',
    'src/sat/smt/pb_pb.cpp',
    'src/sat/smt/pb_solver.cpp',
    'src/sat/smt/q_clause.cpp',
    'src/sat/smt/q_ematch.cpp',
    'src/sat/smt/q_eval.cpp',
    'src/sat/smt/q_mam.cpp',
    'src/sat/smt/q_mbi.cpp',
    'src/sat/smt/q_model_fixer.cpp',
    'src/sat/smt/q_queue.cpp',
    'src/sat/smt/q_solver.cpp',
    'src/sat/smt/q_theory_checker.cpp',
    'src/sat/smt/recfun_solver.cpp',
    'src/sat/smt/sat_th.cpp',
    'src/sat/smt/sls_solver.cpp',
    'src/sat/smt/specrel_solver.cpp',
    'src/sat/smt/tseitin_theory_checker.cpp',
    'src/sat/smt/user_solver.cpp',
    'src/sat/smt/xor_solver.cpp',
    'src/sat/tactic/goal2sat.cpp',
    'src/sat/tactic/sat2goal.cpp',
    'src/sat/tactic/sat_tactic.cpp',
    'src/smt/arith_eq_adapter.cpp',
    'src/smt/arith_eq_solver.cpp',
    'src/smt/dyn_ack.cpp',
    'src/smt/expr_context_simplifier.cpp',
    'src/smt/fingerprints.cpp',
    'src/smt/mam.cpp',
    'src/smt/old_interval.cpp',
    'src/smt/params/dyn_ack_params.cpp',
    'src/smt/params/preprocessor_params.cpp',
    'src/smt/params/qi_params.cpp',
    'src/smt/params/smt_params.cpp',
    'src/smt/params/theory_arith_params.cpp',
    'src/smt/params/theory_array_params.cpp',
    'src/smt/params/theory_bv_params.cpp',
    'src/smt/params/theory_pb_params.cpp',
    'src/smt/params/theory_seq_params.cpp',
    'src/smt/params/theory_str_params.cpp',
    'src/smt/proto_model/proto_model.cpp',
    'src/smt/qi_queue.cpp',
    'src/smt/seq_axioms.cpp',
    'src/smt/seq_eq_solver.cpp',
    'src/smt/seq_ne_solver.cpp',
    'src/smt/seq_offset_eq.cpp',
    'src/smt/seq_regex.cpp',
    'src/smt/smt2_extra_cmds.cpp',
    'src/smt/smt_almost_cg_table.cpp',
    'src/smt/smt_arith_value.cpp',
    'src/smt/smt_case_split_queue.cpp',
    'src/smt/smt_cg_table.cpp',
    'src/smt/smt_checker.cpp',
    'src/smt/smt_clause.cpp',
    'src/smt/smt_clause_proof.cpp',
    'src/smt/smt_conflict_resolution.cpp',
    'src/smt/smt_consequences.cpp',
    'src/smt/smt_context.cpp',
    'src/smt/smt_context_inv.cpp',
    'src/smt/smt_context_pp.cpp',
    'src/smt/smt_context_stat.cpp',
    'src/smt/smt_enode.cpp',
    'src/smt/smt_farkas_util.cpp',
    'src/smt/smt_for_each_relevant_expr.cpp',
    'src/smt/smt_implied_equalities.cpp',
    'src/smt/smt_internalizer.cpp',
    'src/smt/smt_justification.cpp',
    'src/smt/smt_kernel.cpp',
    'src/smt/smt_literal.cpp',
    'src/smt/smt_lookahead.cpp',
    'src/smt/smt_model_checker.cpp',
    'src/smt/smt_model_finder.cpp',
    'src/smt/smt_model_generator.cpp',
    'src/smt/smt_parallel.cpp',
    'src/smt/smt_quantifier.cpp',
    'src/smt/smt_quick_checker.cpp',
    'src/smt/smt_relevancy.cpp',
    'src/smt/smt_setup.cpp',
    'src/smt/smt_solver.cpp',
    'src/smt/smt_statistics.cpp',
    'src/smt/smt_theory.cpp',
    'src/smt/smt_value_sort.cpp',
    'src/smt/tactic/ctx_solver_simplify_tactic.cpp',
    'src/smt/tactic/smt_tactic_core.cpp',
    'src/smt/tactic/unit_subsumption_tactic.cpp',
    'src/smt/theory_arith.cpp',
    'src/smt/theory_array.cpp',
    'src/smt/theory_array_bapa.cpp',
    'src/smt/theory_array_base.cpp',
    'src/smt/theory_array_full.cpp',
    'src/smt/theory_bv.cpp',
    'src/smt/theory_char.cpp',
    'src/smt/theory_datatype.cpp',
    'src/smt/theory_dense_diff_logic.cpp',
    'src/smt/theory_diff_logic.cpp',
    'src/smt/theory_dl.cpp',
    'src/smt/theory_dummy.cpp',
    'src/smt/theory_fpa.cpp',
    'src/smt/theory_lra.cpp',
    'src/smt/theory_opt.cpp',
    'src/smt/theory_pb.cpp',
    'src/smt/theory_recfun.cpp',
    'src/smt/theory_seq.cpp',
    'src/smt/theory_special_relations.cpp',
    'src/smt/theory_str.cpp',
    'src/smt/theory_str_mc.cpp',
    'src/smt/theory_str_regex.cpp',
    'src/smt/theory_user_propagator.cpp',
    'src/smt/theory_utvpi.cpp',
    'src/smt/theory_wmaxsat.cpp',
    'src/smt/uses_theory.cpp',
    'src/smt/watch_list.cpp',
    'src/solver/assertions/asserted_formulas.cpp',
    'src/solver/check_logic.cpp',
    'src/solver/check_sat_result.cpp',
    'src/solver/combined_solver.cpp',
    'src/solver/mus.cpp',
    'src/solver/parallel_tactical.cpp',
    'src/solver/simplifier_solver.cpp',
    'src/solver/smt_logics.cpp',
    'src/solver/solver.cpp',
    'src/solver/solver2tactic.cpp',
    'src/solver/solver_na2as.cpp',
    'src/solver/solver_pool.cpp',
    'src/solver/solver_preprocess.cpp',
    'src/solver/tactic2solver.cpp',
    'src/tactic/aig/aig.cpp',
    'src/tactic/aig/aig_tactic.cpp',
    'src/tactic/arith/add_bounds_tactic.cpp',
    'src/tactic/arith/arith_bounds_tactic.cpp',
    'src/tactic/arith/bv2int_rewriter.cpp',
    'src/tactic/arith/bv2real_rewriter.cpp',
    'src/tactic/arith/degree_shift_tactic.cpp',
    'src/tactic/arith/diff_neq_tactic.cpp',
    'src/tactic/arith/eq2bv_tactic.cpp',
    'src/tactic/arith/factor_tactic.cpp',
    'src/tactic/arith/fix_dl_var_tactic.cpp',
    'src/tactic/arith/fm_tactic.cpp',
    'src/tactic/arith/lia2card_tactic.cpp',
    'src/tactic/arith/lia2pb_tactic.cpp',
    'src/tactic/arith/nla2bv_tactic.cpp',
    'src/tactic/arith/normalize_bounds_tactic.cpp',
    'src/tactic/arith/pb2bv_model_converter.cpp',
    'src/tactic/arith/pb2bv_tactic.cpp',
    'src/tactic/arith/probe_arith.cpp',
    'src/tactic/arith/purify_arith_tactic.cpp',
    'src/tactic/arith/recover_01_tactic.cpp',
    'src/tactic/bv/bit_blaster_model_converter.cpp',
    'src/tactic/bv/bit_blaster_tactic.cpp',
    'src/tactic/bv/bv1_blaster_tactic.cpp',
    'src/tactic/bv/bv_bound_chk_tactic.cpp',
    'src/tactic/bv/bv_bounds_tactic.cpp',
    'src/tactic/bv/bv_size_reduction_tactic.cpp',
    'src/tactic/bv/bvarray2uf_rewriter.cpp',
    'src/tactic/bv/bvarray2uf_tactic.cpp',
    'src/tactic/bv/dt2bv_tactic.cpp',
    'src/tactic/bv/elim_small_bv_tactic.cpp',
    'src/tactic/core/blast_term_ite_tactic.cpp',
    'src/tactic/core/cofactor_elim_term_ite.cpp',
    'src/tactic/core/cofactor_term_ite_tactic.cpp',
    'src/tactic/core/collect_occs.cpp',
    'src/tactic/core/collect_statistics_tactic.cpp',
    'src/tactic/core/ctx_simplify_tactic.cpp',
    'src/tactic/core/der_tactic.cpp',
    'src/tactic/core/elim_term_ite_tactic.cpp',
    'src/tactic/core/elim_uncnstr_tactic.cpp',
    'src/tactic/core/euf_completion_tactic.cpp',
    'src/tactic/core/injectivity_tactic.cpp',
    'src/tactic/core/nnf_tactic.cpp',
    'src/tactic/core/occf_tactic.cpp',
    'src/tactic/core/pb_preprocess_tactic.cpp',
    'src/tactic/core/propagate_values_tactic.cpp',
    'src/tactic/core/reduce_args_tactic.cpp',
    'src/tactic/core/simplify_tactic.cpp',
    'src/tactic/core/special_relations_tactic.cpp',
    'src/tactic/core/split_clause_tactic.cpp',
    'src/tactic/core/symmetry_reduce_tactic.cpp',
    'src/tactic/core/tseitin_cnf_tactic.cpp',
    'src/tactic/dependency_converter.cpp',
    'src/tactic/fd_solver/bounded_int2bv_solver.cpp',
    'src/tactic/fd_solver/enum2bv_solver.cpp',
    'src/tactic/fd_solver/fd_solver.cpp',
    'src/tactic/fd_solver/pb2bv_solver.cpp',
    'src/tactic/fd_solver/smtfd_solver.cpp',
    'src/tactic/fpa/fpa2bv_model_converter.cpp',
    'src/tactic/fpa/fpa2bv_tactic.cpp',
    'src/tactic/fpa/qffp_tactic.cpp',
    'src/tactic/fpa/qffplra_tactic.cpp',
    'src/tactic/goal.cpp',
    'src/tactic/goal_num_occurs.cpp',
    'src/tactic/goal_shared_occs.cpp',
    'src/tactic/goal_util.cpp',
    'src/tactic/portfolio/default_tactic.cpp',
    'src/tactic/portfolio/smt_strategic_solver.cpp',
    'src/tactic/portfolio/solver2lookahead.cpp',
    'src/tactic/portfolio/solver_subsumption_tactic.cpp',
    'src/tactic/probe.cpp',
    'src/tactic/sls/sls_tactic.cpp',
    'src/tactic/smtlogics/nra_tactic.cpp',
    'src/tactic/smtlogics/qfaufbv_tactic.cpp',
    'src/tactic/smtlogics/qfauflia_tactic.cpp',
    'src/tactic/smtlogics/qfbv_tactic.cpp',
    'src/tactic/smtlogics/qfidl_tactic.cpp',
    'src/tactic/smtlogics/qflia_tactic.cpp',
    'src/tactic/smtlogics/qflra_tactic.cpp',
    'src/tactic/smtlogics/qfnia_tactic.cpp',
    'src/tactic/smtlogics/qfnra_tactic.cpp',
    'src/tactic/smtlogics/qfaufbv_tactic.cpp',
    'src/tactic/smtlogics/qfuf_tactic.cpp',
    'src/tactic/smtlogics/qfufbv_ackr_model_converter.cpp',
    'src/tactic/smtlogics/qfufbv_tactic.cpp',
    'src/tactic/smtlogics/smt_tactic.cpp',
    'src/tactic/tactic.cpp',
    'src/tactic/tactical.cpp',
    'src/tactic/smtlogics/qfaufbv_tactic.cpp',
    'src/tactic/ufbv/macro_finder_tactic.cpp',
    'src/tactic/ufbv/quasi_macros_tactic.cpp',
    'src/tactic/ufbv/ufbv_rewriter_tactic.cpp',
    'src/tactic/ufbv/ufbv_tactic.cpp',
    'src/util/approx_nat.cpp',
    'src/util/approx_set.cpp',
    'src/util/bit_util.cpp',
    'src/util/bit_vector.cpp',
    'src/util/cmd_context_types.cpp',
    'src/util/common_msgs.cpp',
    'src/util/debug.cpp',
    'src/util/env_params.cpp',
    'src/util/fixed_bit_vector.cpp',
    'src/util/gparams.cpp',
    'src/util/hash.cpp',
    'src/util/hwf.cpp',
    'src/util/inf_int_rational.cpp',
    'src/util/inf_rational.cpp',
    'src/util/inf_s_integer.cpp',
    'src/util/lbool.cpp',
    'src/util/luby.cpp',
    'src/util/memory_manager.cpp',
    'src/util/min_cut.cpp',
    'src/util/mpbq.cpp',
    'src/util/mpf.cpp',
    'src/util/mpff.cpp',
    'src/util/mpfx.cpp',
    'src/util/mpn.cpp',
    'src/util/mpq.cpp',
    'src/util/mpq_inf.cpp',
    'src/util/mpz.cpp',
    'src/util/page.cpp',
    'src/util/params.cpp',
    'src/util/permutation.cpp',
    'src/util/prime_generator.cpp',
    'src/util/rational.cpp',
    'src/util/region.cpp',
    'src/util/rlimit.cpp',
    'src/util/s_integer.cpp',
    'src/util/scoped_ctrl_c.cpp',
    'src/util/scoped_timer.cpp',
    'src/util/sexpr.cpp',
    'src/util/small_object_allocator.cpp',
    'src/util/smt2_util.cpp',
    'src/util/stack.cpp',
    'src/util/state_graph.cpp',
    'src/util/statistics.cpp',
    'src/util/symbol.cpp',
    'src/util/tbv.cpp',
    'src/util/timeit.cpp',
    'src/util/timeout.cpp',
    'src/util/trace.cpp',
    'src/util/util.cpp',
    'src/util/warning.cpp',
    'src/util/z3_exception.cpp',
    'src/util/zstring.cpp',
    'src/shell/install_tactic.cpp',
    'src/shell/mem_initializer.cpp',
]

z3_inc = [
    'src',
    'src/api',
]

z3_cpp_args = [
    '-std=c++17',
    '-D_EXTERNAL_RELEASE',
    '-DZ3_C_EXAMPLES_FORCE_CXX_LINKER',
    '-DZ3_SINGLE_THREADED',
    '-DZ3_ENABLE_EXAMPLE_TARGETS=OFF',
    '-DZ3_BUILD_EXECUTABLE=OFF',
    '-D_MP_INTERNAL',
    '-DZ3_BUILD_TEST_EXECUTABLE=OFF',
    '-DZ3_BUILD_LIBZ3_SHARED=OFF',
    '-DZ3_LINK_TIME_OPTIMIZATION=ON',
]

libz3 = static_library('z3',
                       z3_src,
                       include_directories: z3_inc,
                       cpp_args: z3_cpp_args,
                       install: false,
)

z3_dep = declare_dependency(
    link_with: libz3,
    include_directories: include_directories(z3_inc)
)
