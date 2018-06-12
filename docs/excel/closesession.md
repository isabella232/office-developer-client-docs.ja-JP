---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798775"
---
# <a name="closesession"></a>CloseSession

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�N���X�^�[�ŃZ�b�V������I�����܂��B
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>�p�����[�^�[

_セッション Id_
  
> �I������Z�b�V������ ID �ł��B���̒l�́A[OpenSession](opensession.md) �ɂ���ĕԂ��ꂽ�l�Ɉ�v����K�v������܂��B
    
## <a name="return-value"></a>�߂�l

�Z�b�V�������I�������ꍇ�� **xlHpcRetSuccess**�A **SessionId** �������������Ȃ��ꍇ�� _xlHpcRetInvalidSessionId_�A���̑��̏�Q�̏ꍇ�� **xlHpcRetCallFailed** �ł��B 
  
## <a name="see-also"></a>�֘A����

- [OpenSession](opensession.md)
- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

