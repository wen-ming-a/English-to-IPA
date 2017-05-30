# IPA Generator (Python 3)
Converts English text to IPA notation

This program utilizes the Carnegie-Mellon University Phonetic Dictionary Database to convert English words into IPA.


    English to IPA
    Word or Phrase: unnaturally
    List of possible transcriptions: 
    1. ənnæʧərəli
    2. ənnæʧərli
    3. ənæʧərli
    4. ənnæʧrəli


#### Some notes and key functions:


* Words which cannot be found in the CMU dictionary are ignored reprinted with an asterisk.
* Stress marking is not currently supported
* **convert(input, retrieve)** - takes a string or list of English text and returns it as a single IPA string. If the **retrieve** parameter is set to 'ALL', a list is instead returned, with all possible combinations of discovered transcriptions returned. 
            
      convert('The quick brown fox jumped over the lazy dog.')
      ðə kwɪk braʊn fɑks ʤəmpt oʊvər ðə lezi dɔg   
* **isin_cmu(word)** - checks if a given word or phrase is in the CMU phonetic dictionary. If a phrase is given, only returns true if all words are in the dictionary. 
* **ipa_list(input)** - returns each transcribed IPA token as a list of all discovered transcriptions.

        ipa_list('The receptionists were busy.')
        [['ði', 'ðə'], ['risɛpʃənɪs', 'risɛpʃənɪsts', 'rɪsɛpʃənɪs', 'rɪsɛpʃənɪsts'], ['wər'], ['bɪzi']]
