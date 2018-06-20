---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798971"
---
# <a name="xlfgetname"></a>xlfGetName

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**定義名**] セクションで [**数式**] タブの **[名前の管理**] をクリックするときに表示される [**名前の管理**] ダイアログ ボックスの**参照先**の列に表示される名前の定義を返します。定義に参照が含まれている場合、それらが r1c1 形式の参照として与えられます。 **XlfGetName**を使用して、名前によって定義された値を確認します。 定義に対応する名前を取得するには、 [xlfGetDef](xlfgetdef.md)を使用します。
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>�p�����[�^�[

_pxNameText_(**xltypeStr**)
  
名前に定義できるシートです。アクティブ ブックに定義された名前への外部参照`"!Sales"`です。特定開いているブックで、たとえば、定義された名前への外部参照、または`"[Book1]SHEET1!Sales"`。  _pxNameText_は、名前は非表示もできます。 
  
_pxInfoType_(**xltypeBool**)
  
���O�ɂ��ĕԂ������̎�ނ�w�肵�܂��B **FALSE** �܂��͏ȗ�����ƁA��**** ����Ă���� **TRUE** ��Ԃ��A���O���u�b�N�S�̂ɑ΂��Ē�`����Ă���� **FALSE** ��Ԃ��܂��B 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxRes_(**xltypeStr**、 **xltypeBool**、または**xltypeErr**)
  
_PxInfoType_に渡される値によって、指定した名前 (**xltypeStr**) または**TRUE**または**FALSE** (**xltypeBool**) の定義を返します。
  
## <a name="remarks"></a>����

**[�V�[�g�̕ی�]** �**�C�A���O �{�b�N�X�� **[�V�[�g�ƃ��b�N���ꂽ�Z���̓�e��ی삷��]** �****#N/A` �G���[�l��Ԃ��܂��B `#N/A` �**�C�A���O �{�b�N�X��\������ɂ́A **[�Z�{]** �^�u�� **[�ύX]** �Z�N�V�����ɂ��� **[�V�[�g�̕ی�]** ��N���b�N���܂��B 
  
���̕\�ɁA�����  **pxNameText** ������w�肵��. _xlfGetDef_ ��Ăяo�����ꍇ�ɕԂ����l�̗�� 3 �����܂��B 
  
|**Excel �ɂ������`**|**_pxNameText_**|**�߂�l**|
|:-----|:-----|:-----|
|�V�[�g�Ŗ��O [Sales] �����l 523 �Ƃ��Ē�`����Ă��܂��B  <br/> |"Sales"  <br/> |"=523"  <br/> |
|�A�N�e�B�u�ȃV�[�g�Ŗ��O [Profit] ���A���� =Sales-Costs �Ƃ��Ē�`����Ă��܂��B  <br/> |"!Profit"  <br/> |"=Sales-Costs"  <br/> |
|�A�N�e�B�u �V�[�g�Ŗ��O [Database] ���A�͈� A1:F500 �Ƃ��Ē�`����Ă��܂��B  <br/> |"!Database"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>�֘A����

- [xlfGetDef](xlfgetdef.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

