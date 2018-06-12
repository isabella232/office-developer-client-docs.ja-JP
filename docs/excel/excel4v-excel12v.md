---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- excel12v function [excel 2007],Excel4v function [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798882"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ���[�N�V�[�g�̓���֐��A�}�N�� �V�[�g�֐���R�}���h�A�܂��� XLL �ŗL�̓���֐���R�}���h�� DLL�AXLL�A�܂��̓R�[�h ���\�[�X�������Ăяo���܂��B
  
Excel �̂��ׂĂ̍ŐV�o�[�W�����́A **Excel4v** ��T�|�[�g���Ă��܂��BExcel 2007 �ȍ~�̃o�[�W�����ł́A **Excel12v** ���T�|�[�g����Ă��܂��B 
  
Excel には、DLL や XLL にコントロールが渡された場合にのみ、これらの関数を呼び出すことができます。 呼び出せるように Excel が経過するとしないコントロール直接に Visual Basic for Applications (VBA)。 他の任意の時点で呼び出すことができません。 たとえば、DllMain 関数またはその他のオペレーティング システムには、DLL が呼び出されたときに、または DLL によって作成されたスレッドからの呼び出し時に呼び出すことはできません。 
  
[Excel4 �� Excel12](excel4-excel12.md) �֐��́A�����̈�����X�^�b�N��̉ϒ����X�g�Ƃ��Ď󂯓���܂��B��� **Excel4v** ����� **Excel12v** �֐��́A�����̈�����z��Ƃ��Ď󂯓���܂��B����ȊO�̂�����_�ɂ����āA **Excel4** �� **Excel4v** �Ɠ����悤�ɓ��삵�A **Excel12** �� **Excel12v** �Ɠ����悤�ɓ��삵�܂��B
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>�p�����[�^�[

 _iFunction_(**int**)
  
�Ăяo���R�}���h�A�֐��A�܂��͓���֐���������l�B _iFunction_ �̗L���Ȓl�̈ꗗ�́A���̉���Q�Ƃ��Ă��������B 
  
 _pxRes_(**LPXLOPER**または**LPXLOPER12**)
  
�]�����ꂽ�֐��̌��ʂ�ێ�����A **XLOPER** ( **Excel4v** �̏ꍇ) �܂��� **XLOPER12** ( **Excel12v** �̏ꍇ) �ւ̃|�C���^�[�B
  
 _iCount_(**int**)
  
�֐��֓n������A�̈����̐��BExcel 2003 �܂ł̃o�[�W�����ł́A0 - 30 �̔C�ӂ̐��ł��BExcel 2007 �ȍ~�́A0 - 255 �̔C�ӂ̐��ł��B
  
 _rgx_(**LPXLOPER**または**LPXLOPER12**)
  
�֐��ւ̈�����܂ޔz��ł��B�z���̂��ׂĂ̈����� **XLOPER** �܂��� **XLOPER12** �̒l�ւ̃|�C���^�[�ł���K�v������܂��B 
  
## <a name="return-value"></a>�߂�l

�����̊֐��́A **Excel4** ����� **Excel12** �Ɠ����l��Ԃ��܂��B
  
## <a name="remarks"></a>����

�����̊֐��́A���Z�q�ɓn���ꂽ�����̐����ς̏ꍇ�ɖ𗧂��܂��B���Ƃ��� **Excel4v** ����� **Excel12v** �́A�����̍��v�����o�^�����֐����������̐��ɂ���Č��܂� [xlfRegister](xlfregister-form-1.md) ��g�p���Ċ֐���o�^����Ƃ��ɖ�ɗ����܂��B **Excel4** �܂��� **Excel12** �̃��b�p�[�֐���L�q����Ƃ��ɂ́A **Excel4v** ����� **Excel12v** ��֗��ł��B�����̏ꍇ�A�ό������X�g��σT�C�Y�̒P��̔z��̈����ɕϊ��� ( **Excel4** �܂��� **Excel12** �֒ʏ�ǂ���񋟂����悤��)�A **Excel4v** �܂��� **Excel12v** ��g�p���� Excel �ɃR�[���o�b�N����K�v������܂��B
  
### <a name="example"></a>��

�R�[�h�̗�ɂ��ẮA���Ɏ��� SDK ��C���X�g�[�������ꏊ�ɂ���AExcel 2010 XLL SDK �� **Excel** ����� **Excel12f** �֐��̃R�[�h��Q�Ƃ��Ă��������B 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>�֘A����



[Excel4�AExcel12](excel4-excel12.md)

