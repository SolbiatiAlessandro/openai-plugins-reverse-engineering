The Speak plugin, as described in your previous message, is designed to assist with language learning and translation tasks. It has three main types of interactions: `translate`, `explainPhrase`, and `explainTask`.

1. `translate`: This is used to translate and explain how to say a specific phrase or word in another language. The fields for this type are:

   - `phrase_to_translate`: The phrase or concept to translate into the foreign language and explain further.
   - `learning_language`: The foreign language that the user is learning and asking about. Always use the full name of the language (e.g. Spanish, French).
   - `native_language`: The user's native language. This value is inferred from the language the user asked their question in. Always use the full name of the language (e.g. Spanish, French).
   - `additional_context`: A description of any additional context in the user's question that could affect the explanation - e.g. setting, scenario, situation, tone, speaking style and formality, usage notes, or any other qualifiers.
   - `full_query`: Full text of the user's question.

2. `explainPhrase`: This is used to explain the meaning and usage of a specific foreign language phrase that the user is asking about. The fields for this type are the same as for `translate`, but with `foreign_phrase` replacing `phrase_to_translate`. The `foreign_phrase` is the foreign language phrase or word that the user wants an explanation for.

3. `explainTask`: This is used to explain the best way to say or do something in a specific situation or context with a foreign language. This is used when the user asks more general or high-level questions. The fields for this type are the same as for `translate`, but with `task_description` replacing `phrase_to_translate`. The `task_description` is a description of the task that the user wants to accomplish or do.

In all cases, the plugin is designed to take into account the full context of the user's question, including the specific language they're asking about, their native language, any additional context that could affect the explanation, and the full text of their question.
