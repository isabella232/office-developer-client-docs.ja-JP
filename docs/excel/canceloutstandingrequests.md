---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798765"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="6a464-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="6a464-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="6a464-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6a464-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6a464-105">Excel Calculation ���������ꂽ���Ƃ�N���X�^�[ �R�l�N�^�ɒʒm���܂��B���̂��߁A���̃Z�b�V�����ɂ����ĕۗ����̊֐��̂��ׂĂ̌Ăяo������������\��������܂� (���� Excel �ł́A���ʂ𔺂��R�[���o�b�N�͕K�v����܂���)�B</span><span class="sxs-lookup"><span data-stu-id="6a464-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="6a464-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6a464-106">Parameters</span></span>

<span data-ttu-id="6a464-107">_セッション Id_</span><span class="sxs-lookup"><span data-stu-id="6a464-107">_SessionID_</span></span>
  
> <span data-ttu-id="6a464-p101">�������ꂽ�v�Z�Ŏg�p����Ă���Z�b�V������ ID �ł��B���̒l�́A[OpenSession](opensession.md) �ɂ���ĕԂ��ꂽ�l�ƈ�v���܂��B</span><span class="sxs-lookup"><span data-stu-id="6a464-p101">The ID of the session used by the canceled calculation. This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a464-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6a464-110">Return value</span></span>

<span data-ttu-id="6a464-111">**SessionId** �������������ꍇ�� _xlHpcRetSuccess_�A **SessionId** �������������Ȃ��ꍇ�� _xlHpcRetInvalidSessionId_�A���̑��̏�Q�̏ꍇ�� **xlHpcRetCallFailed** �ł��B</span><span class="sxs-lookup"><span data-stu-id="6a464-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a464-112">����</span><span class="sxs-lookup"><span data-stu-id="6a464-112">Remarks</span></span>

<span data-ttu-id="6a464-113">���̌Ăяo����Ɏ󂯎�錋�ʂ͂��ׂ� Excel �ɂ���Ĕj������邽�߁A�p�t�H�[�}���X����コ����ɂ́A�������ŃZ�b�V�����̂��ׂẴv���Z�X���~����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6a464-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a464-114">�֘A����</span><span class="sxs-lookup"><span data-stu-id="6a464-114">See also</span></span>

- <span data-ttu-id="6a464-115">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="6a464-115">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

