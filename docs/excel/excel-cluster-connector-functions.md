---
title: Excel �N���X�^�[ �R�l�N�^�֐�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798800"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="09901-103">Excel �N���X�^�[ �R�l�N�^�֐�</span><span class="sxs-lookup"><span data-stu-id="09901-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="09901-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="09901-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="09901-105">Microsoft Excel 2013 �N���X�^�[ �R�l�N�^ DLL �́A���̃Z�N�V�����Ŏ��グ��֐����������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="09901-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="09901-106">���̃Z�N�V�����̎Q�ƃg�s�b�N�Ō��y����Ă���߂�l�́ASDK �C���N���[�h �t�@�C�� (xlcall.h) �Œ�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="09901-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="09901-107">�N���X�^�[ �R�l�N�^�̃A�[�L�e�N�\`��</span><span class="sxs-lookup"><span data-stu-id="09901-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="09901-108">Excel �́A�N���X�^�[ �R�l�N�^�̃G���g�� �|�C���g��Ăяo���āA���[�U�[��\`�֐��Ăяo������p�t�H�[�}���X�̃R���s���[�e�B���O �N���X�^�[�ɓ]�����A�N���X�^�[ �Z�b�V�����Ǘ���s���܂��B</span><span class="sxs-lookup"><span data-stu-id="09901-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="09901-109">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="09901-109">In this section</span></span>

[<span data-ttu-id="09901-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="09901-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="09901-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="09901-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="09901-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="09901-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="09901-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="09901-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="09901-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="09901-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="09901-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="09901-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="09901-116">�֘A����</span><span class="sxs-lookup"><span data-stu-id="09901-116">See also</span></span>



<span data-ttu-id="09901-117">[Excel �N���X�^�[ �R�l�N�^�̊J��](developing-excel-cluster-connectors.md)</span><span class="sxs-lookup"><span data-stu-id="09901-117">[Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md)</span></span>
  
<span data-ttu-id="09901-118">[�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="09901-118">[Cluster Safe Functions](cluster-safe-functions.md)</span></span>

