---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798945"
---
# <a name="showoptions"></a>ShowOptions

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
ユーザーから情報を収集するモーダル ダイアログ ボックスを示しています。 このエントリ ポイントは、ユーザーが ([**数式**] セクションの [**詳細設定**] カテゴリ) は、[ **Excel のオプション**] ダイアログ ボックスで選択したクラスター コネクタの [**クラスターの種類**] ボックスの横の [**オプション**] ボタンをクリックしたときに呼び出されます。 クラスター コネクタは、独自のオプション] ダイアログのインターフェイスを実装して、レジストリや他の場所に関連するデータを格納するために必要があります。 オプションは、クラスター コネクタを内蔵。 Excel が認識ではありません。 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>�p�����[�^�[

_hWndParent_
  
> Excel �E�C���h�E�ւ̃n���h���B
    
## <a name="return-value"></a>�߂�l

�_�C�A���O �{�b�N�X���\�����ꂽ�ꍇ�� **xlHpcRetSuccess**�A�\������Ȃ������ꍇ�� **xlHpcRetCallFailed**�B 
  
## <a name="remarks"></a>����

�N���X�^�[ �R�l�N�^�ł́A�g�p����N���X�^�[ �T�[�o�[�Ȃǂ̏�����[�U�[����擾���邽�߂ɁA���̃_�C�A���O �{�b�N�X��g�p�ł��܂��B
  
## <a name="see-also"></a>�֘A����

- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

