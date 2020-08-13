Replacing text
==================

To find and replace text within a file (using LINUX), use:

.. code-block::

  $ sed -i 's;<OriginalText>;<ReplacementText>;g' <file>.txt

To find and replace text within a file (using MacOS), use:

.. code-block::

  $ sed -i '' 's;<OriginalText>;<ReplacementText>;g' <file>.txt

To rename a large number of files in the same directory all at once, use:

.. code-block::

  $ ls *.fsa
  file1_001.fsa	file2_001.fsa	file3_001.fsa	file4_001.fsa	file5_001.fsa
  file6_001.fsa	file7_001.fsa	file8_001.fsa	file9_001.fsa

.. code-block::

  $ for i in *.fsa; do     mv "$i" "${i//.fsa/.fasta}"; done`

.. code-block::

  $ ls
  file1_001.fasta	file2_001.fasta	file3_001.fasta	file4_001.fasta	file5_001.fasta
  file6_001.fasta	file7_001.fasta	file8_001.fasta	file9_001.fasta

To removed numbers after `_` in a large number of files in the same directory all at once, use:

.. code-block::

  for file in *.fasta; do NEW="`echo $file | awk -F"_" '{print $1}'`.fasta"; mv $file $NEW; done

.. code-block::

  $ ls
  file1.fasta	file2.fasta	file3.fasta	file4.fasta	file5.fasta
  file6.fasta	file7.fasta	file8.fasta	file9.fasta

