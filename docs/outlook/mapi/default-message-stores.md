---
title: ����̃��[���̕ۑ��ꏊ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799871"
---
# <a name="default-message-stores"></a><span data-ttu-id="894c4-103">����̃��[���̕ۑ��ꏊ</span><span class="sxs-lookup"><span data-stu-id="894c4-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="894c4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="894c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="894c4-105">既定のメッセージ ストアは、いずれかの一般的な目的のタスクをメッセージングのクライアント アプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="894c4-105">A default message store is one that client applications can use for general purpose messaging tasks.</span></span> <span data-ttu-id="894c4-106">いくつかのメッセージ ストア プロバイダーは、既定のメッセージ ストアとして使用する場合に必要になるメッセージ ストア プロバイダーの省略可能な機能があります。</span><span class="sxs-lookup"><span data-stu-id="894c4-106">There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store.</span></span> <span data-ttu-id="894c4-107">これは、とおりです。</span><span class="sxs-lookup"><span data-stu-id="894c4-107">They are as follows:</span></span>
  
- <span data-ttu-id="894c4-108">実装の特別なフォルダー: 受信トレイ、送信トレイ、および検索結果のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="894c4-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="894c4-109">�J���� nonread �̃��|�[�g��񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="894c4-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="894c4-110">���M����є��M�������b�Z�[�W�̑��M������܂��B</span><span class="sxs-lookup"><span data-stu-id="894c4-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="894c4-111">�N���X�̔C�ӂ̃��b�Z�[�W����b�Z�[�W�̍쐬������܂��B</span><span class="sxs-lookup"><span data-stu-id="894c4-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="894c4-112">���O�t���ƕ����l�̃v���p�e�B��T�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="894c4-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="894c4-113">メッセージ ストア プロバイダーは、トランスポート プロバイダーと密接に関連があって、 [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="894c4-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="894c4-p102">�֘A����R���e���c�̃e�[�u����T�|�[�g���܂��B�ڍׂɂ��ẮA [�e�[�u���ȓ�e](contents-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="894c4-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="894c4-116">���M���b�Z�[�W�Ƀ��b�Z�[�W������ꍇ�ɁAMAPI �X�v�[���[�̒ʒm��T�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="894c4-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="894c4-117">�֘A����</span><span class="sxs-lookup"><span data-stu-id="894c4-117">See also</span></span>



<span data-ttu-id="894c4-118">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="894c4-118">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

