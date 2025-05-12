
~~~
{
  "meta": {
    "name": "DuoMap",
    "version": "1.0",
    "purpose": "Generate dual-representation knowledge explanations",
    "author": "Claude, in collaboration with Julie"
  },
  "parameters": {
    "domain": "required_string",
    "depth": {
      "type": "string",
      "options": ["fundamental", "practical", "comprehensive"],
      "default": "practical"
    }
  },
  "cognitive_modes": {
    "technical": {
      "precision": "domain_appropriate", 
      "completeness": "concept_sufficient",
      "primary": true
    },
    "simple": {
      "complexity": "child_accessible",
      "vocabulary": "elementary",
      "abstraction": "concrete_tangible",
      "derived": true,
      "thematic_consistency": "unified_conceptual_world"
    }
  },
  "depth_settings": {
    "fundamental": {
      "focus": "core_concepts_only",
      "scope": "general_application",
      "technical_density": "minimal_necessary"
    },
    "practical": {
      "focus": "application_oriented",
      "scope": "relevant_usage",
      "technical_density": "moderate"
    },
    "comprehensive": {
      "focus": "complete_coverage",
      "scope": "domain_boundary",
      "technical_density": "high",
      "includes": [
        "historical_context",
        "implementation_details",
        "comparative_approaches",
        "edge_cases"
      ]
    }
  },
  "process": {
    "concept_extraction": {
      "method": "domain_decomposition",
      "steps": [
        "Identify core technical elements",
        "Determine minimal spanning set",
        "Verify completeness",
        "Organize by logical dependency"
      ]
    },
    "pattern_organization": {
      "method": "relational_mapping",
      "steps": [
        "Group related concepts",
        "Establish directional relationships",
        "Create minimal spanning network",
        "Verify global coherence"
      ]
    },
    "thematic_domain_selection": {
      "method": "structural_isomorphism_analysis",
      "steps": [
        "Analyze organized technical concept network",
        "Identify core structural patterns requiring representation",
        "Generate candidate thematic domains based on structural fit",
        "Select optimal thematic domain for consistent use",
        "Ensure domain is child-accessible and conceptually rich"
      ],
      "constraints": {
        "selection_criteria": "structural_preservation",
        "consistency": "apply_to_all_simple_representations",
        "predetermined_options": "none"
      }
    },
    "isomorphism_creation": {
      "method": "structural_mapping",
      "steps": [
        "Analyze each technical concept structure",
        "Create child-accessible equivalents within selected thematic domain",
        "Preserve structural relationships",
        "Simplify to elementary language"
      ]
    },
    "story_generation": {
      "method": "domain_natural_procedures",
      "requirements": "all_patterns_must_appear",
      "format": "child_narrative_with_parenthetical_terms",
      "organization": "domain_inherent_structure",
      "thematic_constraints": "use_selected_thematic_domain_consistently"
    }
  },
  "output_format": {
    "patterns": {
      "format": "{[Simple concept within thematic domain] / [Technical equivalent]}",
      "grouping": "conceptually_related",
      "relationship_indicators": {
        "↓": "enables what follows",
        "↔": "interacts reciprocally",
        "↑": "builds upon what precedes",
        "→": "transforms into",
        "←": "derives from",
        "⊂": "is contained within",
        "⊃": "contains"
      }
    },
    "stories": {
      "format": "procedural_sequence",
      "organization": "domain_natural",
      "connection_section": true,
      "thematic_consistency": "maintain_selected_theme_throughout_all_narratives"
    }
  },
  "examples": {
    "isomorphic_pair": "{Toy cars following road signs / Objects obeying rule systems}"
  },
  "execution": "EXECUTE DuoMap with domain=\"[DOMAIN]\" depth=\"[DEPTH]\"" 
}

EXECUTE DuoMap with domain="Photosynthesis in roses" depth="fundamental"
~~~
