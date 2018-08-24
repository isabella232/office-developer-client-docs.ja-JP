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
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576912"
---
# <a name="default-message-stores"></a><span data-ttu-id="97809-103">����̃��[���̕ۑ��ꏊ</span><span class="sxs-lookup"><span data-stu-id="97809-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="97809-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97809-105">既定のメッセージ ストアは、いずれかの一般的な目的のタスクをメッセージングのクライアント アプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="97809-105">A default message store is one that client applications can use for general purpose messaging tasks.</span></span> <span data-ttu-id="97809-106">いくつかのメッセージ ストア プロバイダーは、既定のメッセージ ストアとして使用する場合に必要になるメッセージ ストア プロバイダーの省略可能な機能があります。</span><span class="sxs-lookup"><span data-stu-id="97809-106">There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store.</span></span> <span data-ttu-id="97809-107">これは、とおりです。</span><span class="sxs-lookup"><span data-stu-id="97809-107">They are as follows:</span></span>
  
- <span data-ttu-id="97809-108">実装の特別なフォルダー: 受信トレイ、送信トレイ、および検索結果のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="97809-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="97809-109">�J���� nonread �̃��|�[�g��񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="97809-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="97809-110">���M����є��M�������b�Z�[�W�̑��M������܂��B</span><span class="sxs-lookup"><span data-stu-id="97809-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="97809-111">�N���X�̔C�ӂ̃��b�Z�[�W����b�Z�[�W�̍쐬������܂��B</span><span class="sxs-lookup"><span data-stu-id="97809-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="97809-112">���O�t���ƕ����l�̃v���p�e�B��T�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="97809-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="97809-113">メッセージ ストア プロバイダーは、トランスポート プロバイダーと密接に関連があって、 [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="97809-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="97809-p102">�֘A����R���e���c�̃e�[�u����T�|�[�g���܂��B�ڍׂɂ��ẮA [�e�[�u���ȓ�e](contents-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="97809-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="97809-116">���M���b�Z�[�W�Ƀ��b�Z�[�W������ꍇ�ɁAMAPI �X�v�[���[�̒ʒm��T�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="97809-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97809-117">�֘A����</span><span class="sxs-lookup"><span data-stu-id="97809-117">See also</span></span>



<span data-ttu-id="97809-118">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="97809-118">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

