---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798992"
---
# <a name="xlfgetdef"></a>xlfGetDef

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
テキストで特定の領域、値、またはブック内の数式で定義されている名前を返します。 Excel では、この値を取得する使用**xlfGetDef**の [**数式**] タブで**定義された名前**] セクションで **[名前の管理**] をクリックするときに表示される [**名前の管理**] ダイアログ ボックスの [**名前**] 列で、定義に対応する名前です。 名前の定義を取得するには、 [xlfGetName](xlfgetname.md)を使用します。
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>�p�����[�^�[

_pxDefText_(**xltypeStr**)
  
�Q�ƁA�l�A�I�u�W�F�N�g�A�����ȂǁA�Q�Ɛ�̖��O�Ƃ��Ē�`�ł��邠�����̂�w��ł��܂��B
  
�Q�Ƃ̏ꍇ�́A `"R3C5"` �Ȃǂ� R1C1 �X�^�C���Ŏw�肷��K�v������܂��B  _pxDefText_ ���l�܂��͐����̏ꍇ�A **[���O�̊Ǘ�]** �_�C�A���O �{�b�N�X�� **[�Q�Ɣ͈�]** ��ɕ\������铙�� (=) ��܂߂�K�v�͂���܂���B  _pxDefText_ �ɕ����̖��O�����݂���ꍇ�A **xlfGetDef** �͍ŏ��̖��O��Ԃ��܂��B  _pxDefText_ �ƈ�v���閼�O�����݂��Ȃ��ꍇ�A **xlfGetDef** ��  `#NAME?` �G���[�l��Ԃ��܂��B 
  
_pxDocumentText_(**xltypeStr**)
  
_pxDefText_ �����݂���V�[�g��w�肵�܂��B  _pxDocumentText_ ���ȗ������ƁA�A�N�e�B�u�ȃV�[�g�Ƃ��đz�肳��܂��B 
  
_pxTypeNum_(**xltypeNum**)
  
�Ԃ����O�̎�ނ�w�肷��A1 ���� 3 �͈̔͂̐��l�ł��B
  
|**_pxTypeNum_**|**�߂�l**|
|:-----|:-----|
|1 �܂��͏ȗ�  <br/> |�W�����̂݁B  <br/> |
|2  <br/> |��\�����̂݁B  <br/> |
|3  <br/> |���ׂĂ̖��O�B  <br/> |
   
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 _pxRes_(**xltypeStr**または**xltypeErr**)
  
�w��̒�`�Ɋ֘A�t�����Ă��閼�O��Ԃ��܂��B
  
## <a name="remarks"></a>����

���̕\�ɁA����̈�����w�肵�� **xlfGetDef** ��Ăяo�����ꍇ�ɕԂ����l�̗�� 4 �����܂��B 
  
|**Excel �Œ�`���ꂽ���O**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**�߂�l**|
|:-----|:-----|:-----|:-----|:-----|
|Sheet4 �̎w��͈̔͂ɂ́uSales�v�Ƃ������O���t���Ă��܂��B  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"Sales"  <br/> |
|Sheet4 �̒l 100 �́A�uConstant�v�Ƃ��Ē�`����Ă��܂��B  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"Constant"  <br/> |
|Sheet4 �̎w��̐����ɂ́uSumTotal�v�Ƃ������O���t���Ă��܂��B  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<�ȗ�\>  <br/> |"SumTotal"  <br/> |
|�A�N�e�B�u�ȃV�[�g�̔�\�����uCounter�v�Ƃ��� 3 ����`����Ă��܂��B  <br/> |"3"  <br/> |\<�ȗ�\>  <br/> |2  <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>�֘A����

- [xlfGetName](xlfgetname.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

