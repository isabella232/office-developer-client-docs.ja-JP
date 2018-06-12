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
# <a name="closesession"></a><span data-ttu-id="ac526-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="ac526-103">CloseSession</span></span>

<span data-ttu-id="ac526-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ac526-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ac526-105">�N���X�^�[�ŃZ�b�V������I�����܂��B</span><span class="sxs-lookup"><span data-stu-id="ac526-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="ac526-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ac526-106">Parameters</span></span>

<span data-ttu-id="ac526-107">_セッション Id_</span><span class="sxs-lookup"><span data-stu-id="ac526-107">_SessionId_</span></span>
  
> <span data-ttu-id="ac526-p101">�I������Z�b�V������ ID �ł��B���̒l�́A[OpenSession](opensession.md) �ɂ���ĕԂ��ꂽ�l�Ɉ�v����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="ac526-p101">The ID of the session to close. This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac526-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ac526-110">Return value</span></span>

<span data-ttu-id="ac526-111">�Z�b�V�������I�������ꍇ�� **xlHpcRetSuccess**�A **SessionId** �������������Ȃ��ꍇ�� _xlHpcRetInvalidSessionId_�A���̑��̏�Q�̏ꍇ�� **xlHpcRetCallFailed** �ł��B</span><span class="sxs-lookup"><span data-stu-id="ac526-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac526-112">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ac526-112">See also</span></span>

- [<span data-ttu-id="ac526-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="ac526-113">OpenSession</span></span>](opensession.md)
- <span data-ttu-id="ac526-114">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="ac526-114">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

