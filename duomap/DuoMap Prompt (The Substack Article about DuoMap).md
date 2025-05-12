(yeah, during revision, some of this was changed, so this may not be using the FINAL final article... still, it illustrates the use case)

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

EXECUTE DuoMap with DOMAIN=[the Substack draft article below] and DEPTH=["PRACTICAL"]


---BEGIN ARTICLE---
This semantic operator is one of my favorites.

And, it has a long history.

LLMs contain quite the storehouse of information, and all at your fingertips. But extracting that knowledge in a useful way can be tricky.

In the beginning, I leaned heavily on a bot’s ELI5 capabilities to simplify an unknown notion when I started a new knowledge journey. That helped a LOT. But when I started applying it more broadly, things started to get out of hand. I got linear outputs of stuff, like a classroom experience on fast forward. I could not see the interconnections between core topics. Sometimes, I could not see the core topics at all, since they were buried in the pile. And refining my prompts to “surface the core topics and show their interrelationships” worked a bit better, but it didn’t always include ALL of them. And, what if I wanted to go deeper? Like, in a fractal manner? Ugh.

So I decided to see if my semantic operators could help. And they did.

After spending a couple of months on a predecessor version called Eigenfeed (big, mathy, and… well, still unsatisfying), I went back to the drawing board and spelled out my core requirements for the operator.

- ask the LLM to gather the domain’s core topics on its own (meaning, no templates) and ensures that the set is complete;
    
- let the LLM determine the interrelationships between the topics;
    
- have the LLM pick a suitable thematic domain, generating ELI7 mode renditions of the topics from this domain, and then “knit” them together with the original technical terms;
    
- output the topic “constellation” and then tell an ELI7 story about them (with the technical notions added as parentheticals).
    

The result was DuoMap: the amazing “Knowledge-O-Matic.” And at just under 4K (about ), it is WAY smaller than the 16K Eigenfeed ancestor.

Interested? DuoMap is on my [GitHub repository](https://github.com/jmgustasson/semanticky/tree/main/duomap).

Here’s a lightly edited output from a sample run:

---

`DuoMap: HTTPS Protocol`

`Patterns & Relationships`

`{Secure Postal Service / HTTPS Protocol}   ↓   {Sealed Envelopes / TLS Encryption}   ↔ {Secret Code Books / SSL Certificates}   ↓   {Verified Stamps / Digital Signatures}`

`{Post Office System / TCP/IP Network}   ↓   {Mailbox Numbers / IP Addresses}   ↔ {Office Door Numbers / Port Numbers}   → {Address Labels / Domain Names}`

`{Mail Sorting Process / DNS Resolution}   ← {Phonebook Lookup / DNS Query}   ↑ {Directory Service / DNS Server}`

`{Letter Exchange Rules / Protocol Handshake}   ⊂ {Opening Ceremony / TLS Handshake}   → {Secret Handshakes / Key Exchange}   → {Permission Slips / Session Keys}`

`Connection Story: Building the Secure Postal Network`

`In our special postal town, every building has both a mailbox number (IP address) and an office door number (port number). When you want to send secure mail, you use the Secure Postal Service (HTTPS), which always delivers to door 443.`

`Before sending anything private, the post office performs an opening ceremony (TLS handshake). First, they exchange secret code books (SSL certificates) to verify identities. Then they create unique permission slips (session keys) for that specific delivery.`

`To find the right building, the postal service uses a phonebook lookup (DNS query) through the directory service (DNS server). This mail sorting process (DNS resolution) turns friendly building names into exact mailbox numbers.`

`Once connected, all letters travel in sealed envelopes (TLS encryption) with verified stamps (digital signatures). The secret handshakes (key exchange) ensure only the intended recipient can open the envelope.`

`This entire system runs on the regular post office network (TCP/IP), but adds special security rules. Every step follows strict letter exchange rules (protocol handshake) to keep messages safe from interception.`

---

The prompt to run DuoMap is very simple:

`EXECUTE DuoMap with domain="HTTPS Protocol" depth="practical"`

### So… what else can I run this on?

[

![Anakin This Is Where The Fun Begins : r/MemeTemplatesOfficial](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30e3c8be-268c-41a9-877e-80ecfd67bf1e_605x358.jpeg "Anakin This Is Where The Fun Begins : r/MemeTemplatesOfficial")



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30e3c8be-268c-41a9-877e-80ecfd67bf1e_605x358.jpeg)

Well, I’ve run it on:

- long web pages (those that aren’t bot-protected) that you don’t have the time to read
    
- attached documents (your own, or someone else’s) - does a pretty good job of generating a survey of the material (but the LLM will “supplement” the information with its own; this may or may not be desirable)
    
- chat sessions (as a rough “gauge” of the overall flow… YMMV here)
    

While coming up with examples for DuoMap, I realized that the most powerful capability of DuoMap might be its ability to analyze what you’ve written.

Let’s see how it does with this Substack article:
---END ARTICLE---
~~~

