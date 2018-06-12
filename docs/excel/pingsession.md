---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798951"
---
# <a name="pingsession"></a><span data-ttu-id="738f5-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="738f5-103">PingSession</span></span>

<span data-ttu-id="738f5-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="738f5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="738f5-p101">�Z�b�V�������L�����ǂ�����\`�F�b�N���܂��B���̊֐��͒ʏ�A�ȑO�Ԃ��ꂽ�Z�b�V���� ID �����݂�A�N�e�B�u�Ŏg�p�\���ǂ����� Excel �Ŕ��f����K�v������ꍇ�ɌĂяo����܂��B</span><span class="sxs-lookup"><span data-stu-id="738f5-p101">Checks whether a session is valid. This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="738f5-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="738f5-107">Parameters</span></span>

<span data-ttu-id="738f5-108">_セッション Id_</span><span class="sxs-lookup"><span data-stu-id="738f5-108">_SessionID_</span></span>
  
> <span data-ttu-id="738f5-p102">ping ����s����Z�b�V������ ID �B���̒l�́A�O�� [OpenSession](opensession.md) ��Ăяo�����ۂɕԂ��ꂽ ID �ƈ�v����K�v������܂� �B</span><span class="sxs-lookup"><span data-stu-id="738f5-p102">The ID of the session to ping. This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="738f5-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="738f5-111">Return value</span></span>

<span data-ttu-id="738f5-112">**SessionId** �������L���̏ꍇ�� _xlHpcRetSuccess_�A����ȊO�̏ꍇ�� **xlHpcRetInvalidSessionId**�B</span><span class="sxs-lookup"><span data-stu-id="738f5-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="738f5-113">�֘A����</span><span class="sxs-lookup"><span data-stu-id="738f5-113">See also</span></span>

- [<span data-ttu-id="738f5-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="738f5-114">OpenSession</span></span>](opensession.md)
- <span data-ttu-id="738f5-115">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="738f5-115">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

