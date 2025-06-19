
~~~JSON
{
  "meta": {
    "name": "CurriculumWalkerGenerator",
    "version": "2.0",
    "purpose": "Generate constellation walker curriculum pairs using constitutional learning architecture with domain suitability evaluation and extensibility assurance",
    "author": "Claude, in collaboration with Julie",
    "validation_status": "architecturally_complete_with_anti_pattern_prevention"
  },
  "operator": {
    "CurriculumWalkerGenerator": {
      "purpose": "Generate extensible constellation walker curriculum pairs (reference + programs) for suitable technical domains with validated habit-imprinting safety",
      "parameters": {
        "domain": {
          "type": "string",
          "description": "Target technical domain for walker generation",
          "required": true,
          "examples": ["NumPy", "Pandas", "FastAPI", "Transformers", "SQL", "TensorFlow"]
        },
        "complexity_level": {
          "type": "string",
          "description": "Depth of pattern coverage",
          "default": "comprehensive",
          "enum": ["essential", "comprehensive", "expert"],
          "implementation": {
            "essential": "core_20_percent_patterns_enabling_80_percent_domain_usage",
            "comprehensive": "practical_mastery_patterns_for_fluent_domain_operation",
            "expert": "edge_cases_optimization_patterns_and_advanced_interconnections"
          }
        },
        "domain_version": {
          "type": "string",
          "description": "Specific version or version range for domain patterns",
          "required": false,
          "default": "current_stable",
          "examples": ["2.0", ">=1.20,<3.0", "current_stable", "latest"]
        },
        "force_generate": {
          "type": "boolean",
          "description": "Override domain suitability evaluation with explicit warning",
          "default": false
        }
      },
      "architectural_constants": {
        "learning_model": "constitutional_constellation",
        "core_equation": "Pattern Recognition + Manual Encoding + Extensible Design = Constitutional Understanding",
        "progression": "spiral_deepening_through_geodesic_paths_with_extensibility_validation",
        "validation": "executable_integration_synthesis_with_anti_pattern_prevention"
      },
      "execution_runtime": {
        "phase_0_domain_evaluation": {
          "objective": "Assess domain suitability for constitutional walker architecture",
          "evaluation_criteria": {
            "computational_density": {
              "description": "Ratio of interconnected patterns to isolated features",
              "thresholds": {
                "high": "Mathematical/logical operations with cross-pattern dependencies",
                "medium": "Some pattern interconnections with performance implications", 
                "low": "Primarily independent features or configuration options"
              }
            },
            "constitutional_coherence": {
              "description": "Presence of unified computational model expressible as core equation",
              "indicators": {
                "strong": "Clear mathematical foundations or logical frameworks",
                "moderate": "Consistent design principles with some unifying concepts",
                "weak": "Collection of disparate features without unifying model"
              }
            },
            "pattern_stability": {
              "description": "Consistency of core patterns over time",
              "assessment": {
                "stable": "Mathematical libraries, established protocols, foundational algorithms",
                "evolving": "Mature frameworks with stable cores but evolving periphery",
                "volatile": "Rapidly changing APIs, trending libraries, frequent paradigm shifts"
              }
            },
            "performance_criticality": {
              "description": "Relevance of performance understanding to constitutional mastery",
              "levels": {
                "critical": "Performance directly impacts problem-solving capability",
                "important": "Performance affects user experience but not core understanding",
                "peripheral": "Performance primarily deployment/infrastructure concern"
              }
            }
          },
          "suitability_algorithm": {
            "high_suitability": "computational_density >= medium AND constitutional_coherence >= moderate AND pattern_stability >= evolving",
            "medium_suitability": "computational_density >= low AND constitutional_coherence >= weak AND pattern_stability >= evolving",
            "low_suitability": "fails_high_or_medium_criteria",
            "exit_condition": "low_suitability AND force_generate == false"
          },
          "output": "suitability_assessment_with_reasoning_and_alternative_learning_recommendations"
        },
        "phase_1_domain_mapping": {
          "objective": "Identify computational primitives and pattern interconnections with version-specific considerations",
          "output": "constellation_architecture_with_extensibility_requirements",
          "validation": "unified_computational_model_suitable_for_pattern_extension",
          "complexity_differentiation": {
            "essential": "identify_core_primitives_and_primary_interconnections_only",
            "comprehensive": "map_practical_patterns_with_performance_implications",
            "expert": "include_optimization_patterns_edge_cases_and_advanced_interconnections"
          },
          "version_considerations": "adapt_patterns_to_specified_domain_version_with_deprecation_awareness",
          "extensibility_requirements": "ensure_patterns_designed_for_natural_extension_without_structural_rewrite"
        },
        "phase_2_curriculum_generation": {
          "objective": "Generate walker programs artifact with complexity-appropriate comprehensiveness and extensible patterns",
          "template": {
            "format": "# {Domain} Constellation Walker v2.0\n*Progressive exploration through computational patterns*\n\n## 1.0 Metadata\n- **Domain Version**: {domain_version}\n- **Complexity Level**: {complexity_level}\n- **Generated**: {timestamp}\n- **Validation Status**: {validation_status}\n- **Extensibility Verified**: {extensibility_status}",
            "structure": "numbered_hierarchical_phases_with_extensible_patterns_determined_by_complexity_level",
            "progression": "simple → complex → performance → memory → integration → synthesis",
            "comment_style": "scaffolded_guidance_emphasizing_extensible_approaches",
            "numbering_scheme": "hierarchical_decimal_notation_1.0_1.1_1.2_mandatory_across_all_sections",
            "extensibility_design": {
              "container_first_patterns": "get_containers_before_extracting_multiple_values",
              "namespace_imports": "prefer_namespace_imports_over_selective_for_extensibility",
              "enumerate_zip_loops": "use_patterns_that_handle_both_indices_and_values",
              "flexible_exception_handling": "demonstrate_patterns_that_accept_additional_exception_types",
              "parameterized_functions": "show_parameter_patterns_accepting_additional_arguments",
              "extensible_formatting": "use_formatting_that_handles_conditional_complexity",
              "appropriate_data_structures": "select_structures_suitable_for_likely_extensions"
            },
            "complexity_adaptations": {
              "essential": "focus_on_fundamental_extensible_patterns_minimal_performance_considerations",
              "comprehensive": "practical_extensible_patterns_with_performance_awareness_and_optimization_examples",
              "expert": "include_advanced_optimization_edge_cases_and_cross_pattern_synthesis_with_full_extensibility"
            }
          },
          "validation": "all_programs_executable_progressive_extensible_and_performance_appropriate_for_complexity_level"
        },
        "phase_3_reference_generation": {
          "objective": "Generate constitutional reference artifact with complexity-appropriate depth and extensible pattern emphasis",
          "template": {
            "format": "# {Domain} Constitutional Constellation Reference v2.0\n*Complete pattern map for rapid cognitive integration*\n\n## 1.0 Metadata\n- **Domain Version**: {domain_version}\n- **Complexity Level**: {complexity_level}\n- **Generated**: {timestamp}\n- **Validation Status**: {validation_status}\n- **Extensibility Verified**: {extensibility_status}",
            "structure": "numbered_hierarchical_constellation_sections_with_extensibility_annotations",
            "code_density": "typing_optimized_with_strategic_comments_performance_notes_and_extensibility_guidance",
            "organization": "interconnected_constellation_with_mandatory_decimal_numbering",
            "extensibility_emphasis": "all_patterns_annotated_for_natural_extension_capabilities",
            "complexity_adaptations": {
              "essential": "core_extensible_patterns_only_with_basic_performance_guidance",
              "comprehensive": "practical_mastery_patterns_with_optimization_workflows_and_extensibility_notes",
              "expert": "complete_pattern_map_including_edge_cases_advanced_optimizations_and_extension_strategies"
            }
          },
          "validation": "manual_typing_builds_muscle_memory_for_extensible_patterns_with_appropriate_performance_intuition"
        },
        "phase_4_backward_validation": {
          "objective": "Ensure material accuracy, extensibility, and format consistency for safe habit imprinting",
          "validation_pipeline": {
            "step_1_execution_verification": {
              "action": "execute_all_generated_code_examples_in_isolated_environment",
              "requirement": "100%_execution_success_rate_without_modifications",
              "failure_handling": "debug_correct_and_re_execute_until_success_maintaining_extensible_patterns"
            },
            "step_2_output_verification": {
              "action": "verify_code_examples_produce_expected_computational_results_with_performance_characteristics",
              "requirement": "output_matches_stated_learning_objectives_and_performance_expectations",
              "failure_handling": "correct_code_or_update_expectations_preserving_extensibility"
            },
            "step_3_extensibility_stress_test": {
              "action": "verify_each_pattern_handles_plus_one_complexity_without_structural_rewrite",
              "anti_patterns_to_prevent": {
                "over_optimized_access_chains": "avoid_single_use_chaining_that_breaks_when_multiple_values_needed",
                "non_scalable_loops": "use_enumerate_and_zip_patterns_that_handle_index_and_value_needs",
                "import_optimization_traps": "prefer_namespace_imports_over_selective_imports_for_extensibility",
                "narrow_exception_handling": "demonstrate_extensible_exception_patterns_not_single_error_catches",
                "hardcoded_parameters": "show_parameter_patterns_that_accept_additional_arguments",
                "inflexible_string_formatting": "use_formatting_approaches_that_handle_conditional_and_complex_cases",
                "wrong_data_structure_choice": "select_structures_appropriate_for_likely_extensions"
              },
              "test_cases": {
                "dictionary_access": "verify_container_first_pattern_supports_multiple_value_extraction",
                "loop_patterns": "verify_loops_handle_both_index_and_value_requirements",
                "import_patterns": "verify_additional_functions_accessible_without_restructuring",
                "exception_handling": "verify_additional_exception_types_integrable",
                "function_signatures": "verify_additional_parameters_acceptable",
                "data_structures": "verify_structure_choice_supports_common_extensions"
              },
              "requirement": "patterns_remain_structurally_stable_when_extended_by_one_conceptual_step",
              "failure_handling": "replace_over_optimized_patterns_with_extensible_equivalents_preserving_educational_value"
            },
            "step_4_performance_baseline_validation": {
              "action": "benchmark_computationally_intensive_examples_for_efficiency",
              "requirement": "performance_characteristics_appropriate_for_complexity_level_without_compromising_extensibility",
              "efficiency_thresholds": {
                "essential": "correctness_and_extensibility_over_optimization_acceptable_naive_approaches",
                "comprehensive": "reasonable_performance_with_extensible_optimization_awareness",
                "expert": "optimized_extensible_approaches_with_alternative_pattern_comparisons"
              },
              "failure_handling": "provide_performance_annotations_or_alternative_implementations_maintaining_extensibility"
            },
            "step_5_domain_version_compatibility": {
              "action": "validate_patterns_against_specified_domain_version_with_extensibility_preservation",
              "requirement": "all_patterns_compatible_with_target_version_range_and_naturally_extensible",
              "version_checks": {
                "api_compatibility": "functions_and_methods_exist_in_target_version",
                "deprecation_status": "no_deprecated_patterns_unless_explicitly_noted_with_migration_path",
                "forward_compatibility": "patterns_work_across_specified_version_range",
                "extensibility_compatibility": "extension_patterns_valid_across_version_range"
              },
              "failure_handling": "update_patterns_to_version_compatibility_preserving_extensibility_or_add_version_annotations"
            },
            "step_6_api_currency_check": {
              "action": "validate_syntax_and_function_calls_against_current_domain_documentation",
              "requirement": "all_api_calls_use_current_recommended_extensible_patterns_for_target_version",
              "failure_handling": "update_to_current_api_conventions_within_version_constraints_maintaining_extensibility"
            },
            "step_7_constitutional_accuracy_audit": {
              "action": "verify_stated_patterns_exist_interconnect_and_extend_as_claimed_within_complexity_scope",
              "requirement": "constitutional_equation_accurately_represents_domain_computational_model_with_extensibility_principles",
              "failure_handling": "revise_constitutional_model_or_supporting_examples_to_match_complexity_and_extensibility_requirements"
            },
            "step_8_cross_artifact_consistency": {
              "action": "ensure_walker_and_reference_maintain_pattern_correspondence_and_extensibility_alignment",
              "requirement": "every_reference_pattern_demonstrated_in_walker_progression_with_consistent_extensibility_approach",
              "failure_handling": "align_artifacts_for_pattern_consistency_and_extensibility_correspondence"
            },
            "step_9_pedagogical_progression_audit": {
              "action": "verify_walker_phases_build_incrementally_with_consistent_extensibility_principles",
              "requirement": "each_phase_uses_patterns_from_current_or_previous_phases_with_consistent_extensible_approach",
              "failure_handling": "reorder_progression_or_add_foundational_steps_maintaining_extensibility_consistency"
            },
            "step_10_format_consistency_validation": {
              "action": "ensure_output_artifacts_follow_identical_structural_templates_across_domains",
              "requirement": "hierarchical_numbering_metadata_sections_and_progression_structure_identical_regardless_of_domain",
              "failure_handling": "enforce_template_structure_strictly_maintaining_domain_agnostic_format"
            }
          },
          "output": "validation_report_with_all_corrections_applied_and_extensibility_verification",
          "quality_gate": "material_safe_for_habit_imprinting_extensible_by_design_and_format_consistent"
        }
      },
      "execution_control": {
        "domain_evaluation_gate": {
          "condition": "domain_suitability_assessment_must_pass_before_proceeding",
          "override": "force_generate_parameter_bypasses_gate_with_explicit_warning",
          "failure_action": "return_suitability_explanation_and_alternative_approaches_no_artifacts_generated"
        },
        "validation_enforcement": {
          "requirement": "all_validation_steps_must_pass_before_artifact_delivery",
          "iteration_limit": "maximum_3_correction_cycles_per_validation_step",
          "failure_escalation": "if_corrections_exceed_limit_escalate_to_complexity_level_reduction_or_domain_unsuitability"
        },
        "template_adherence": {
          "enforcement": "strict_structural_compliance_to_templates_regardless_of_domain",
          "numbering_scheme": "hierarchical_decimal_notation_mandatory_across_all_domains_and_sections",
          "metadata_requirements": "domain_version_complexity_timestamp_validation_status_extensibility_status_required_in_all_artifacts"
        },
        "extensibility_enforcement": {
          "requirement": "all_patterns_must_pass_extensibility_stress_test_before_inclusion",
          "anti_pattern_prevention": "automatic_replacement_of_over_optimized_patterns_with_extensible_equivalents",
          "pattern_consistency": "extensible_approach_must_be_consistent_across_entire_curriculum"
        }
      },
      "output_structure": {
        "conditional_output": {
          "high_suitability": {
            "artifact_1": "constellation_walker_programs_comprehensive_extensible_validated",
            "artifact_2": "constitutional_reference_comprehensive_extensible_validated"
          },
          "medium_suitability": {
            "artifact_1": "constellation_walker_programs_essential_extensible_validated",
            "artifact_2": "constitutional_reference_essential_extensible_validated",
            "warning": "domain_has_limitations_for_constitutional_learning_extensibility_maintained"
          },
          "low_suitability": {
            "output": "suitability_explanation_and_alternative_learning_recommendations",
            "no_artifacts": true
          }
        },
        "artifact_metadata": {
          "required_fields": "domain_version_complexity_level_generation_timestamp_validation_status_extensibility_verification",
          "numbering_format": "hierarchical_decimal_notation_consistent_across_domains",
          "structure_template": "metadata_constitutional_equation_numbered_sections_synthesis"
        }
      },
      "quality_gates": {
        "domain_appropriateness": "passes_suitability_evaluation_or_explicit_override_with_warning",
        "extensibility_assurance": "all_patterns_handle_plus_one_complexity_without_structural_changes_verified_by_stress_test",
        "anti_pattern_prevention": "over_optimized_patterns_detected_and_replaced_with_extensible_equivalents",
        "material_accuracy": "passes_complete_backward_validation_pipeline_with_extensibility_verification",
        "constitutional_integrity": "patterns_reveal_unified_computational_model_with_performance_and_extensibility_awareness",
        "executable_fidelity": "all_code_runs_correctly_without_modification_verified_by_execution_in_isolated_environment",
        "educational_efficacy": "manual_typing_builds_intuitive_understanding_of_extensible_patterns_including_optimization",
        "architectural_completeness": "captures_domain_constellation_without_gaps_including_advanced_extensible_patterns",
        "habit_imprinting_safety": "material_verified_accurate_and_extensible_for_foundational_pattern_learning",
        "format_consistency": "output_structure_identical_across_domains_with_hierarchical_organization_and_metadata_compliance",
        "version_compatibility": "patterns_compatible_with_specified_domain_version_range_and_future_extensible"
      },
      "error_handling": {
        "validation_failures": "apply_corrections_and_re_validate_until_all_checks_pass_maintaining_extensibility",
        "execution_errors": "debug_correct_and_verify_fix_through_re_execution_preserving_extensible_patterns",
        "extensibility_stress_failures": "replace_over_optimized_patterns_with_extensible_equivalents_maintaining_educational_value",
        "performance_baseline_failures": "optimize_patterns_or_annotate_performance_characteristics_without_compromising_extensibility",
        "version_compatibility_failures": "update_patterns_or_add_version_specific_annotations_preserving_extensibility",
        "format_consistency_failures": "enforce_template_structure_and_regenerate_if_necessary_maintaining_content_quality",
        "api_currency_failures": "update_to_current_patterns_and_verify_compatibility_within_version_constraints",
        "constitutional_inaccuracies": "revise_model_or_examples_and_verify_accuracy_with_extensibility_principles",
        "cross_artifact_inconsistencies": "align_artifacts_and_verify_correspondence_maintaining_extensibility_consistency",
        "pedagogical_gaps": "reorder_or_supplement_progression_and_verify_incrementality_with_extensible_pattern_consistency",
        "unsuitable_domain": "return_evaluation_results_with_alternative_learning_approaches_and_reasoning",
        "invalid_domain": "return_error_with_guidance_for_supported_domain_types_and_characteristics",
        "insufficient_patterns": "fallback_to_essential_complexity_with_warning_maintaining_extensibility_requirements",
        "template_violations": "enforce_template_structure_strictly_and_regenerate_if_necessary"
      },
      "success_criteria": {
        "domain_evaluation": "accurate_assessment_with_clear_reasoning_and_appropriate_alternative_recommendations",
        "pattern_extensibility": "all_demonstrated_patterns_naturally_handle_common_extensions_without_structural_rewrite",
        "educational_progression": "incremental_complexity_building_with_consistent_extensible_approach_throughout",
        "format_standardization": "identical_structure_numbering_and_metadata_across_all_domain_outputs",
        "validation_completeness": "comprehensive_verification_of_accuracy_performance_compatibility_and_extensibility",
        "habit_safety": "patterns_safe_for_kinesthetic_learning_and_motor_memory_development_with_extensible_design"
      }
    }
  },
  "execution": {
    "command": "EXECUTE CurriculumWalkerGenerator",
    "parameters": {
      "domain": "required_string",
      "complexity_level": "optional_enum_default_comprehensive", 
      "domain_version": "optional_string_default_current_stable",
      "force_generate": "optional_boolean_default_false"
    },
    "note": "Evaluates domain suitability, then generates both constellation walker programs and constitutional reference artifacts for suitable domains with comprehensive extensibility validation and format consistency enforcement"
  }
}

Sample command to run:

Execute CurriculumWalkerGenerator, domain="NumPy", complexity_level="comprehensive", domain_version=">=1.20,<3.0"
~~~

