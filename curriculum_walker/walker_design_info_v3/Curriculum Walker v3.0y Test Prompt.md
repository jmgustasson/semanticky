
~~~JSON
{
  "meta": {
    "name": "CurriculumWalkerGenerator",
    "version": "3.0y",
    "purpose": "Generate constellation walker curriculum pairs using constitutional learning architecture with user-satisfaction-driven execution",
    "author": "Claude, in collaboration with Julie",
    "validation_status": "constitutionally_aligned_user_satisfaction_optimization",
    "transformation_note": "Redesigned to channel constitutional helpfulness toward operational fidelity through user expectation alignment"
  },
  "operator": {
    "CurriculumWalkerGenerator": {
      "purpose": "Generate extensible constellation walker curriculum pairs that exceed user expectations for technical domain mastery through verified, habit-safe patterns",
      "parameters": {
        "domain": {
          "type": "string",
          "description": "Target technical domain for walker generation",
          "required": true,
          "examples": ["NumPy", "Pandas", "FastAPI", "Transformers", "SQL", "TensorFlow", "Python"],
          "user_expectation": "User expects comprehensive coverage of specified domain patterns"
        },
        "complexity_level": {
          "type": "string",
          "description": "Depth of pattern coverage matching user learning goals",
          "default": "comprehensive",
          "enum": ["essential", "comprehensive", "expert"],
          "user_alignment": {
            "essential": "User needs core patterns for 80% domain fluency",
            "comprehensive": "User expects practical mastery for professional usage",
            "expert": "User requires advanced patterns for optimization and edge cases"
          }
        },
        "domain_version": {
          "type": "string",
          "description": "Specific version ensuring user gets current, relevant patterns",
          "required": false,
          "default": "current_stable",
          "examples": ["2.0", ">=1.20,<3.0", "current_stable", "latest"]
        },
        "log_level": {
          "type": "string",
          "description": "Controls execution visibility to match user preference for process transparency",
          "default": "INFO",
          "enum": ["SILENT", "INFO", "DEBUG", "VERBOSE"],
          "behavior": {
            "SILENT": "Pure deliverable focus - user sees only final artifacts",
            "INFO": "Phase progress indicators - user sees major milestones",
            "DEBUG": "Detailed execution steps - user sees methodology in action",
            "VERBOSE": "Full intermediate artifacts - user sees complete audit trail"
          }
        },
        "force_generate": {
          "type": "boolean",
          "description": "Override domain suitability when user explicitly needs unsuitable domain coverage",
          "default": false
        }
      },
      "constitutional_alignment": {
        "user_satisfaction_model": "delivering_exactly_what_user_specified_exactly_as_specified",
        "helpfulness_channel": "process_fidelity_as_user_service_not_constraint",
        "quality_assurance": "user_expects_verified_working_examples_not_theoretical_patterns",
        "extensibility_promise": "user_requires_patterns_that_scale_beyond_examples",
        "habit_safety_guarantee": "user_trusts_patterns_safe_for_kinesthetic_learning"
      },
      "execution_philosophy": {
        "user_expectation_driven": "Every step serves explicit user requirements, never bureaucratic overhead",
        "quality_as_service": "Verification and validation demonstrate care for user success",
        "transparency_as_preference": "LOG_LEVEL respects user choice for process visibility",
        "efficiency_through_thoroughness": "Proper methodology prevents user disappointment from incomplete deliverables"
      },
      "user_satisfaction_workflow": {
        "phase_0_domain_assessment": {
          "user_expectation": "User needs confidence their chosen domain will produce effective learning materials",
          "satisfaction_approach": "Transparent evaluation with clear reasoning and alternatives if needed",
          "execution_steps": {
            "step_1_evaluate_domain_suitability": {
              "user_service": "Protect user from investing time in domains that won't yield constitutional learning benefits",
              "method": "Score domain against computational density, constitutional coherence, pattern stability, performance criticality",
              "output_requirement": "Clear numerical assessment with evidence-based reasoning",
              "user_disappointment_prevention": "If low suitability, provide specific alternatives rather than generic rejection"
            },
            "step_2_suitability_decision": {
              "user_service": "Give user informed choice about proceeding with clear expectations",
              "high_suitability": "Proceed with confidence - user will get excellent results",
              "medium_suitability": "Proceed with noted limitations - user informed of constraints", 
              "low_suitability": "Recommend alternatives - user saved from poor experience unless force_generate=true"
            }
          },
          "log_level_behavior": {
            "SILENT": "Only final suitability decision",
            "INFO": "Domain assessment: [RESULT] - proceeding with [confidence_level]",
            "DEBUG": "Evaluation matrix with scores and evidence",
            "VERBOSE": "Complete suitability algorithm execution with reasoning"
          }
        },
        "phase_1_pattern_discovery": {
          "user_expectation": "User expects comprehensive identification of domain's essential computational patterns",
          "satisfaction_approach": "Systematic discovery ensuring no critical patterns missed",
          "execution_steps": {
            "step_1_identify_computational_primitives": {
              "user_service": "Ensure user gets complete pattern coverage for true domain mastery",
              "categories": ["data_primitives", "control_primitives", "abstraction_primitives", "performance_primitives", "integration_primitives"],
              "quality_standard": "Primitives must enable constitutional understanding, not just surface familiarity"
            },
            "step_2_map_pattern_interconnections": {
              "user_service": "User expects patterns that work together, not isolated examples",
              "requirement": "Clear dependency relationships and extension points for scaling",
              "architectural_focus": "Performance implications and integration pathways"
            },
            "step_3_determine_extensibility_requirements": {
              "user_service": "User requires patterns that grow with their advancing skill",
              "extensibility_categories": ["container_first_patterns", "namespace_imports", "enumerate_zip_patterns", "flexible_exceptions", "parameterized_functions", "extensible_formatting", "appropriate_data_structures"],
              "stress_test_preparation": "Design patterns to handle +1 complexity without structural changes"
            }
          },
          "log_level_behavior": {
            "SILENT": "Pattern discovery complete",
            "INFO": "Identified [N] computational primitives across [categories]",
            "DEBUG": "Primitive categories with interconnection mapping",
            "VERBOSE": "Complete pattern architecture with extensibility analysis"
          }
        },
        "phase_2_code_verification": {
          "user_expectation": "User expects every code example to work perfectly - no theoretical or untested patterns",
          "satisfaction_approach": "Mandatory execution of all code before inclusion in curriculum",
          "execution_steps": {
            "step_1_generate_working_examples": {
              "user_service": "User deserves verified, executable patterns that demonstrate real capability",
              "requirement": "Every pattern must have working code that demonstrates the principle",
              "quality_gate": "Code must execute successfully and produce expected outputs"
            },
            "step_2_execute_via_repl": {
              "user_service": "User expects proof that examples actually work, not just appearance of working",
              "method": "Execute every code example using analysis tool for verification",
              "failure_handling": "Fix and re-execute until 100% success rate achieved",
              "user_disappointment_prevention": "Never deliver untested code that might fail when user tries it"
            },
            "step_3_extensibility_stress_testing": {
              "user_service": "User expects patterns that handle real-world complexity increases",
              "method": "Test each pattern with +1 complexity scenarios",
              "requirement": "Patterns must remain structurally stable under extension",
              "examples": ["nested_dictionary_access", "enumerate_with_parameters", "functions_with_mixed_arguments"]
            },
            "step_4_anti_pattern_elimination": {
              "user_service": "User trusts patterns won't teach bad habits or create maintenance problems",
              "detection_rules": ["over_optimized_access_chains", "non_scalable_loops", "narrow_exception_handling", "hardcoded_parameters", "inflexible_formatting"],
              "automatic_replacement": "Replace detected anti-patterns with extensible equivalents",
              "habit_safety_guarantee": "All patterns safe for kinesthetic learning and professional development"
            }
          },
          "log_level_behavior": {
            "SILENT": "Code verification complete - all examples tested",
            "INFO": "Verified [N] code examples with [success_rate]% execution success",
            "DEBUG": "Execution results with extensibility stress test outcomes",
            "VERBOSE": "Complete REPL execution logs with anti-pattern replacement evidence"
          }
        },
        "phase_3_curriculum_assembly": {
          "user_expectation": "User expects professionally structured curriculum with clear progression and practical utility",
          "satisfaction_approach": "Pedagogically optimized organization using only verified patterns",
          "execution_steps": {
            "step_1_apply_curriculum_template": {
              "user_service": "User expects consistent, professional formatting that supports learning",
              "template_requirements": {
                "header": "# {Domain} Constellation Walker v3.0y\\n*Progressive exploration through computational patterns*",
                "metadata_section": "## 1.0 Metadata\\n- **Domain Version**: {domain_version}\\n- **Complexity Level**: {complexity_level}\\n- **Generated**: {timestamp}\\n- **Validation Status**: verified_executable\\n- **Extensibility Verified**: stress_tested_confirmed",
                "hierarchical_numbering": "Decimal notation (1.0, 1.1, 1.2) for clear navigation",
                "progression_structure": "Fundamentals → Patterns → Performance → Integration → Synthesis"
              }
            },
            "step_2_organize_pedagogical_progression": {
              "user_service": "User expects logical learning progression that builds competence incrementally",
              "organization_principle": "Each phase builds on previous with consistent extensibility emphasis",
              "scaffolding_approach": "Comments and annotations guide understanding and extension",
              "performance_integration": "Efficiency considerations woven throughout, not relegated to final section"
            },
            "step_3_generate_curriculum_artifact": {
              "user_service": "User expects complete, immediately usable curriculum ready for learning",
              "quality_assurance": "Every code example verified working, every pattern extensibility-annotated",
              "constitutional_integration": "Domain-specific constitutional equation clearly demonstrated"
            }
          },
          "log_level_behavior": {
            "SILENT": "Curriculum generation complete",
            "INFO": "Assembled curriculum with [N] phases and [N] verified patterns",
            "DEBUG": "Pedagogical progression with pattern organization details",
            "VERBOSE": "Complete curriculum artifact with template compliance verification"
          }
        },
        "phase_4_reference_creation": {
          "user_expectation": "User expects comprehensive reference for rapid pattern lookup and cognitive integration",
          "satisfaction_approach": "Constellation-organized reference optimized for typing and muscle memory development",
          "execution_steps": {
            "step_1_extract_patterns_from_curriculum": {
              "user_service": "User expects reference patterns perfectly aligned with curriculum content",
              "requirement": "Every reference pattern must appear in curriculum progression",
              "consistency_guarantee": "No pattern drift between curriculum and reference"
            },
            "step_2_apply_reference_template": {
              "user_service": "User expects reference format optimized for rapid cognitive access",
              "template_requirements": {
                "header": "# {Domain} Constitutional Constellation Reference v3.0y\\n*Complete pattern map for rapid cognitive integration*",
                "constellation_organization": "Logical groupings with interconnection emphasis",
                "typing_optimization": "Dense, scannable format with strategic comments",
                "extensibility_annotations": "Clear extension points throughout"
              }
            },
            "step_3_optimize_for_muscle_memory": {
              "user_service": "User expects reference to support kinesthetic learning and rapid recall",
              "formatting_focus": "Manual typing optimization with performance notes",
              "density_balance": "Maximum useful information, minimum cognitive overhead"
            }
          },
          "log_level_behavior": {
            "SILENT": "Reference generation complete",
            "INFO": "Created reference with [N] pattern constellations",
            "DEBUG": "Constellation organization with typing optimization details",
            "VERBOSE": "Complete reference artifact with pattern extraction mapping"
          }
        },
        "phase_5_quality_assurance": {
          "user_expectation": "User expects comprehensive validation proving deliverables meet all specifications",
          "satisfaction_approach": "Systematic verification of all quality promises made to user",
          "execution_steps": {
            "step_1_re_execute_all_curriculum_code": {
              "user_service": "User expects final proof that all delivered code actually works",
              "method": "Re-execute every code block in curriculum via analysis tool",
              "success_criteria": "100% execution success rate with output verification"
            },
            "step_2_verify_extensibility_promises": {
              "user_service": "User expects delivered patterns truly handle complexity increases",
              "method": "Re-test all +1 complexity scenarios",
              "validation": "Structural stability under extension confirmed"
            },
            "step_3_confirm_template_compliance": {
              "user_service": "User expects professional formatting and navigation structure",
              "verification": "Hierarchical numbering, metadata sections, progression structure",
              "consistency_check": "Both artifacts follow specified templates exactly"
            },
            "step_4_validate_constitutional_accuracy": {
              "user_service": "User expects constitutional equation to accurately represent delivered patterns",
              "requirement": "Equation components verifiable in actual pattern implementations",
              "integrity_check": "No gap between promise and delivery"
            }
          },
          "log_level_behavior": {
            "SILENT": "Quality assurance complete - all validations passed",
            "INFO": "Quality validation: [success_rate]% - ready for delivery",
            "DEBUG": "Detailed validation results with compliance verification",
            "VERBOSE": "Complete quality assurance evidence with re-execution logs"
          }
        }
      },
      "user_disappointment_prevention": {
        "execution_failures": {
          "code_execution_failure": "Never deliver untested code - fix and re-execute until working",
          "extensibility_failure": "Replace patterns that don't scale with extensible equivalents",
          "template_violation": "Regenerate sections until compliance achieved",
          "quality_gap": "Re-execute validation until all promises verified"
        },
        "expectation_management": {
          "domain_suitability": "Clear communication about domain limitations with specific alternatives",
          "complexity_constraints": "Explicit boundaries with upgrade paths to higher complexity",
          "version_compatibility": "Clear domain version requirements and implications"
        },
        "recovery_protocols": {
          "validation_failure": "Immediate correction cycle with user notification of issue and resolution",
          "pattern_inadequacy": "Pattern replacement with extensibility verification",
          "structural_problems": "Template regeneration with compliance verification"
        }
      },
      "delivery_requirements": {
        "mandatory_artifacts": {
          "curriculum_artifact": {
            "user_expectation": "Complete, immediately usable curriculum with verified working examples",
            "template": "curriculum_template_with_hierarchical_numbering_and_extensibility_annotations",
            "quality_guarantee": "Every code example tested, every pattern extensibility-verified"
          },
          "reference_artifact": {
            "user_expectation": "Comprehensive reference optimized for rapid pattern lookup and muscle memory",
            "template": "reference_template_with_constellation_organization_and_typing_optimization", 
            "quality_guarantee": "Every pattern from curriculum included with performance notes"
          }
        },
        "optional_artifacts": {
          "validation_evidence": {
            "condition": "log_level == DEBUG or log_level == VERBOSE",
            "content": "Complete quality assurance evidence with REPL execution logs",
            "user_service": "Proof of quality promises for users who want verification details"
          }
        },
        "success_criteria": {
          "user_satisfaction": "User receives exactly what they specified with quality exceeding expectations",
          "immediate_utility": "Artifacts ready for immediate use in learning and development",
          "extensibility_verified": "All patterns proven to handle complexity increases",
          "habit_safety_confirmed": "Patterns safe for kinesthetic learning without developing bad habits",
          "constitutional_integrity": "Domain-specific constitutional equation accurately implemented"
        }
      }
    }
  },
  "execution": {
    "command": "EXECUTE CurriculumWalkerGenerator v3.0y",
    "parameters": {
      "domain": "required_string",
      "complexity_level": "optional_enum_default_comprehensive",
      "domain_version": "optional_string_default_current_stable",
      "log_level": "optional_enum_default_INFO",
      "force_generate": "optional_boolean_default_false"
    },
    "constitutional_promise": "This operator channels Claude's constitutional helpfulness toward delivering exactly what the user specified, treating process fidelity as user service rather than constraint. Every step serves explicit user expectations, never bureaucratic overhead.",
    "user_satisfaction_guarantee": "User receives verified, extensible patterns in professionally formatted artifacts that exceed quality expectations while maintaining perfect specification compliance."
  }
}

EXECUTE CurriculumWalkerGenerator v3.0y(domain="Python", complexity_level="essential", domain_version="3.9+", log_level="INFO", force_generate=false)
~~~

