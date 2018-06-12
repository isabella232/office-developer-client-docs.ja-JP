---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798938"
---
# <a name="opensession"></a>OpenSession

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���[�U�[��`�֐�����s�ł���Z�b�V������쐬���܂��B
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>�p�����[�^�[

_Params_
  
> �Z�b�V�����̃p�����[�^�[�́A�Z�~�R�����ŋ�؂�ꂽ UNICODE ������ւ̃|�C���^�[�BExcel �ł́A���̈����͎g�p���܂���B
    
## <a name="return-value"></a>�߂�l

�Z�b�V����������ɍ쐬���ꂽ�ꍇ�́A���̃N���X�^�[ �R�l�N�^�ɑ΂��鑼�̌Ăяo���Ŏg�p����Z�b�V���� ID�B����ȊO�̏ꍇ�� **xlHpcRetCallFailed**�B
  
## <a name="see-also"></a>�֘A����

- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

