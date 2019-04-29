---
title: Excel ���[�N�V�[�g�Ǝ��̕]��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427767"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Excel ワークシートと式の評価

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel ���[�N�V�[�g�̃Z���̓�e�́A���� 4 �̊�{�I�ȃf�[�^�^�̂����ꂩ�ɕ]������܂��B
  
- **Numbers**
    
- **Boolean TRUE** �܂��� **FALSE**
    
- **Strings**
    
- **Errors**
    
�֐��̈����Ƃ��āA�܂��͔z�񐔎���̕����̃Z���ɂ܂�����l�Ƃ��āA�����̃f�[�^�^�̍����z��𐔎��ɓ��͂��邱�Ƃ�ł��܂��B
  
���[�U�[ (�܂��̓R�}���h �}�N��) ���Z���ɕ��������͂���ƁAExcel �͓��͂̉�߂���݁A��߂ł��Ȃ��ꍇ�ɂ̓G���[ ���b�Z�[�W��\�����܂��B���͒l��������̃v���t�B�b�N�X (�P����p��) �Ŏn�܂��Ă���ꍇ�́AExcel �́A���ׂĂ̓��͕�������̂܂ܕύX�����ɃZ���ɔz�u���܂��B(������̃v���t�B�b�N�X�͕\������܂���B)���͒l���A **=** �A **+** �A **-** �̂����ꂩ�Ŏn�܂�ꍇ�AExcel �͓��͒l�𐔎��Ƃ��ĉ�߂��悤�Ƃ��܂��B�\�����������Ȃ��ꍇ��]������~�����ꍇ�́A�G���[���\������A�Z���͕ҏW���[�h�ɂȂ�܂��B����ȊO�̏ꍇ�AExcel �͉��Z�q����ъ֐����Ƃ��̈����̎��ʁA�ϊ��A�]������݂܂��B 
  
���Z�q���K�p�����O�ɁA�I�y�����h�͍�����E�ɕ]������܂��B�֐��́A�D�揇�ʂ̍������Z�q�Ɠ���q�̈�ԓ���̉��Z�q����]������܂��B�֐��̈�����I�y�����h���A�\�������f�[�^�^�ɕϊ��ł��Ȃ��ꍇ�A�]���͎��s���A **#VALUE!** �G���[�ɂȂ�܂��B�g�[�N�� (���e�����l�ł͂Ȃ�) ���֐������`���A���x���Ƃ��ĔF������Ȃ��ꍇ�A�]���͎��s���A **#NAME?** �G���[�ɂȂ�܂��B 
  
���͒l����L�̂�����ł�n�܂��Ă��Ȃ��ꍇ�́A���t�A�����A�ʉ݁A�p�[�Z���e�[�W�A���l�ȂǁA���m�̓��̓p�^�[���ɏƂ炵�ă`�F�b�N���A�����ɉ����ĉ�߂���܂��B����́A���P�[���ŗL�̕��@�ōs���܂��B��L�̂�����̕��@�ł��߂ł��Ȃ��ꍇ�́A������Ƃ��ĔF����������A�Z���̓�e�͕ύX����܂���B
  
Excel �͑��̃f�[�^�^��T�|�[�g���Ă���A���̒��ōł�悭�m���Ă���̂́A�͈͎Q�Ƃł��B�Q�ƈ�����Ƃ�Ȃ����Z�q��֐��̈�����]��������A�܂��̓Z���̐�����ɂ��鎮��Q�Ƃɏk�߂��肷��ƁA�Q�Ƃ͎Q�Ɛ�Z���̒l�ɕϊ�����܂��B
  
Excel �ł́AXLM �֐� **EVALUATE** �܂��͂���ɑ������� C API�֐� **xlfEvaluate** ��g���āA�L���ȕ������A���[�N�V�[�g�p�̊�{�I�� 4 �̃f�[�^�^�̂����ꂩ�ɏk�߂�@�\�����J����Ă��܂��B���ł���̊֐���g�p����ƁADLL �R�[�h��̖��O�t���͈͂�ȒP�ɕ]�����邱�Ƃ��ł��܂��B���̊֐��́A�G���[���b�Z�[�W��\��������A�Z���̕ҏW��\�ɂ����肷��̂ł͂Ȃ��A���̕]�����ł��Ȃ��ꍇ�� **#VALUE!** �G���[��Ԃ��Ƃ����_�ŁA�O�q�̓���Ƃ͈قȂ�܂��B 
  
## <a name="numbers"></a>数値

Excel のワークシート番号はすべて、8 バイトの倍精度浮動小数点 (すべての整数を含む) で内部的に表されます。ただし、Excel におけるこれらの数値の実装は、以下の表に示すように、IEEE 規格に完全には準拠していません。
  
|**�^**|**�ő�**|**�ŏ�**|
|:-----|:-----|:-----|
|IEEE 8 �o�C�g�̔{���x���������_�^  <br/> |1.7976931348623157 e + 308  <br/> |2.2250738585072014 e-308  <br/> |
|���[�N�V�[�g (�֐��܂��͓\��t���l�ɂ���ĕԂ����)  <br/> |1.7976931348623157 e + 308  <br/> |2.22507385850721 e-308  <br/> |
|���[�N�V�[�g (�葀�����)  <br/> |9.99999999999999 e + 307  <br/> |2.22507385850721 e-308  <br/> |
   
IEEE �񐳋K���� ( 2.2250738585072009E?308 ���� 4.9406564584124654E?324 �͈̔͂̐��l) �́AExcel ���[�N�V�[�g�ł̓T�|�[�g����Ă��܂��񂪁AVBA �̔{���x���������_�^�ł̓T�|�[�g����Ă��܂��B
  
If a DLL function returns IEEE +/- infinity or an invalid double, Excel converts it to **#NUM!**. All subnormal numbers and numbers smaller than the minimum positive normal in Excel are converted to positive zero. IEEE negative zero is supported, that is, it can be returned by a DLL function and is displayed as **-0**. (The **\<** operator does not check for negative zero, and so **=A1\<0** evaluates to **TRUE** if A1 contains negative zero). 
  
���t�Ǝ����Ȃǂ̈ꕔ�̐��l�����́A��L��������͈͂ɐ�������Ă��邱�Ƃɒ��ӂ��Ă��������B�������Z�͎��ۂɂ͕��������_���Z�ł���A�ɒ[�ȏꍇ�́A���m�ɂ͐����̌��ʂɂȂ�ꍇ�ɔ񐮐��̌��ʂ����炷�ꍇ������܂��B
  
## <a name="long-unicode-strings"></a>長い Unicode 文字列

���݁AExcel ��ɕ\������Ă��镶����͂��ׂāA�����̃o�[�W�����ɂ����āA����I�� Unicode ������Ƃ��Ċi�[����܂��B���[�N�V�[�g�Ŏg�p���� Unicode ������ł́A�C�ӂ̗L���� Unicode ������ő� 32,767 (2<sup>15</sup>?- 1) �����܂ނ��Ƃ��ł��܂��B 
  
C API ���ŏ��ɓ������ꂽ�Ƃ��A���[�N�V�[�g�̕�����́A���� 255 �����̃o�C�g��ɐ�������Ă��܂������AC API �ł�A�����̐��������f����܂��BExcel 2007 �ł́AC API �́A���� Unicode �����������ł���悤�ɍX�V����Ă��܂��B�܂�ADLL �֐����K�؂ȕ��@�œo�^����Ă���΁AUnicode �̈�����󂯎������AUnicode �������Ԃ����肷�邱�Ƃ��ł��܂��B
  
> [!NOTE]
> バイト列は、下位互換性のために C API で完全にサポートされていますが、これまでどおり 255 文字に制限されています。 
  
## <a name="returning-errors"></a>エラー

関数または演算子の引数を適切な型に変換できない場合、あるいは関数または定義済みの名前が認識されない場合、Excel はセルをエラーに評価します。これらのシナリオはいずれも上記で説明しています。組み込みワークシート関数と演算子が失敗した場合、ユーザーにエラーの種類を通知するエラーも表示されます。自作のアドイン関数が Excel の動作と整合するエラーを返すようにしてください。
  
### <a name="null"></a>#NULL!

**#NULL!** �G���[�́A�������� XLM ���֐��ɂ���ĕԂ���܂��B���Ƃ��΁A�v�����^�[���C���X�g�[������Ă��Ȃ��ꍇ�ɁA **GET.DOCUMENT(78)** ��Ăяo�����A�܂��͈��� 78 �œ����� C API �֐� **xlfGetDocument** ��Ăяo���ƁA���̃G���[���Ԃ���邱�ƂɂȂ�܂��B�܂��A��L�G���[�͋�̕����񂪕]�������ꍇ�Ȃǂɂ�A�ꕔ�̊֐��ŕԂ����\��������܂��B 
  
他のいずれのエラーも適切ではないと感じる場合も、アドイン関数からこのエラーを返すとよいでしょう。
  
### <a name="div0"></a>#DIV/0!

���ꂪ 0 �ɕ]������邩�A�܂��͐��l�������� 0 �ȊO�̐��l�ŕ\���Ȃ��ꍇ�ɂ́AExcel �̏��Z���Z�q�� **#DIV/0!** �G���[��Ԃ��܂��B��`��A���Z���֌W����ꕔ�̊֐��ł���̃G���[���Ԃ����ꍇ������܂��B���Ƃ��΁A���͒l�̂��������l�ɕϊ��ł��Ȃ��ꍇ�́A **AVERAGE** �ɂ�肱�̃G���[���Ԃ���܂��B 
  
0 による除算が検出されたことを示す場合にのみ、アドイン関数からこのエラーが返されるようにしてください。
  
### <a name="value"></a>#VALUE!

**#VALUE!** �G���[�́A�֐��܂��͉��Z�q�̈������K�v�Ȍ^�ɕϊ��ł��Ȃ��ꍇ�ɕԂ���܂��B�ϊ��ł��Ȃ��֐��̈��� (��F  `=LN("X")`) �̏ꍇ �A�֐��R�[�h�͌Ăяo����܂���B����́A�Ǝ��̃A�h�C���֐��̍쐬��f�o�b�O��s���ۂɏd�v�ȃ|�C���g�ł��B 
  
�������̊֐��ł́A�֐��R�[�h��ň�����ϊ��ł��Ȃ��ꍇ�ɂ��̃G���[���Ԃ���܂��B���Ƃ��΁A `DATEVALUE("30-Feb-2007")` �͐������^�̈����ł���ɂ������炸�A���̃G���[�𔺂��Ď��s���܂��B���̏ꍇ�A���̊֐��ɂ���Ċ֐��R�[�h�����G���[���Ԃ���܂��B�l�̌^��͈͂����e�͈͂ł����Ă�A�֐��ɂ���Ă͂��̃G���[���Ԃ���܂��B���Ƃ��΁A  `FIND("a","xyz")` �͂��̃G���[��Ԃ��܂��B 
  
������������^�ł��邱�Ƃ�A�������^�ɕϊ��ł��Ȃ��������ƁA�͈͊O�ł��邱�Ƃ�������߂ɁA�A�h�C���֐�����G���[��Ԃ��悤�ɂ��Ă��������B�������A���l�̈������͈͊O�̏ꍇ�� **#NUM!** ��Ԃ��悤�������Ă��������B�͈͂�z������̃T�C�Y��`���قȂ�ꍇ�ɂ�A���̃G���[��Ԃ��悤�������Ă��������B 
  
### <a name="ref"></a>#REF!

���ʓI�ɑ��ΎQ�Ƃ͈̔͊O�̏ꏊ�ɃR�s�[�����ƁA����� **#REF!** �G���[����������܂��B���Ƃ��΁AB2 �Z���ɐ���  `=A1` �������Ă���ꍇ�AB1 �Z���ɂ��̐�����R�s�[����ƁA���ʂ͐��� **=#REF!** �ɂȂ�܂��B���̃G���[�́A�؂���/�\��t������ŏ㏑�����ꂽ�Q�Ƃ�A���s�A���[�N�V�[�g���ƍ폜���ꂽ�Q�Ƃ������Ɋ܂܂��ꍇ�ɂ��������܂��B  `OFFSET(A1,-1,-1)` �ȂǁA�Q�Ƃ�Ԃ��������̊֐��͂��̃G���[��Ԃ��\��������܂��B���[�N�V�[�g���̒�`�ɁA�����ƂȂ�Q�Ƃ��܂܂�Ă���ꍇ�́A���̃G���[�ɕ]������܂��B
  
�A�h�C���֐����Q�ƈ��������Ă��āA�Q�Ƃ������ł��邩�A�܂��͎Q�ƃG���[��ʂ����ꍇ�́A���̃G���[��Ԃ��悤�������Ă��������B[Excel �̃������Ǘ�](memory-management-in-excel.md)�� XLOPER/XLOPER12 �Z�N�V�����ł́A�Q�ƈ�����󂯎��A�Ԃ����Ƃ��ł���֐���쐬������@�ɂ��Đ�����Ă��܂��B 
  
### <a name="name"></a>#NAME?

Excel generates the **#NAME?** error when an expression contains a token that is not recognized as a function or defined name. If your add-in function tries to access a defined name and it is not defined, you should consider returning this error. 
  
### <a name="num"></a>#NUM!

Excel の組み込みの数値および数学関数の多くは、#NUM を返します **。** 数値の入力が許容範囲外の場合に、エラーが発生し`LN(0)`ます (例:)。 数値入力が無効または範囲外であることを示すため、アドイン関数からこのエラーを返すよう検討してください。
  
### <a name="na"></a>#N/A

�����̏ꍇ **#N/A** �G���[�́A����Ȍ��ʂ܂��͗L���Ȍ��ʂ����p�ł��Ȃ����Ƃ�\���܂��B���Ƃ��΁A���S��v��������Ȃ������ꍇ�ɂ́A�� 3 ������ 0 �� MATCH �֐���肱�̃G���[���Ԃ���܂��B�܂��A���̃G���[�́A�֐� **NA** ��g�p���A�֐� **ISNA** �ŌʂɌ��o���āA�������邱�Ƃ�ł��܂��B���̂��߁A���̃G���[�́A�A�v���P�[�V�����ŗL�̏���͈͂�������߂Ƀ��[�N�V�[�g�ň�ʓI�Ɏg�p����Ă��܂��B
  
## <a name="see-also"></a>関連項目



[Excel プログラミングの概念](excel-programming-concepts.md)
  
[Excel �ł� C API ��g�p�����v���O���~���O](programming-with-the-c-api-in-excel.md)
  
[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)

