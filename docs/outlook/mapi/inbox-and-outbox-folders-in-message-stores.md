---
title: ��M�g���C ���b�Z�[�W �X�g�A��̃t�H���_�[�����M�g���C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2bd71ee4fca53fbf3d309cbaf9d33835b84c0c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801061"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a><span data-ttu-id="e7b2f-103">��M�g���C ���b�Z�[�W �X�g�A��̃t�H���_�[�����M�g���C</span><span class="sxs-lookup"><span data-stu-id="e7b2f-103">Inbox and Outbox Folders in Message Stores</span></span>

  
  
<span data-ttu-id="e7b2f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7b2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7b2f-105">既定のメッセージ ストアには、メッセージ ストア プロバイダーは受信トレイを実装し、フォルダーを [送信トレイ] する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-105">To be the default message store, a message store provider must implement Inbox and Outbox folders.</span></span> <span data-ttu-id="e7b2f-106">通常メッセージ ストアの IPM サブツリーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-106">They are typically stored in the IPM subtree of a message store.</span></span> <span data-ttu-id="e7b2f-107">これらのフォルダーは、特別な特別な機能のこれらの必要はありませんがメッセージを配信してから送信されたフォルダーとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-107">These folders are special in that they are designated as the folders that messages are delivered to and sent from, but no special functionality is required of them.</span></span> <span data-ttu-id="e7b2f-108">クライアント アプリケーションとの間、MAPI スプーラーでは、メッセージ ストア プロバイダーの定義済みの呼び出しシーケンスを使用してメッセージの送受信が行われます。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-108">Sending and receiving messages happens by way of defined call sequences between client applications, the MAPI spooler, and the message store provider.</span></span> <span data-ttu-id="e7b2f-109">単なるものの中にメッセージを保持するために使用されているフォルダー、受信トレイ、送信トレイ フォルダーのシーケンスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-109">The Inbox and Outbox folders are simply folders that are used to hold messages during those call sequences.</span></span> <span data-ttu-id="e7b2f-110">重要なポイントはフォルダーは、特別なまたは受信トレイと送信トレイはその名前が偶数ではありません。重要なポイントは、メッセージ ストア プロバイダーは、そのサポートの一環としてメッセージを送受信するためです。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-110">The important point is not that the folders are special, or even that they are named Inbox and Outbox; the important point is that the message store provider uses them as part of its support for sending and receiving messages.</span></span>
  
<span data-ttu-id="e7b2f-111">メッセージの受信をサポートするには、メッセージ ストア プロバイダーは、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドと[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)メソッドを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-111">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods.</span></span> <span data-ttu-id="e7b2f-112">詳細については、[メッセージ ストア プロバイダーを使用してメッセージの受信](receiving-messages-by-using-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-112">For more information, see [Receiving Messages by Using Message Store Providers](receiving-messages-by-using-message-store-providers.md).</span></span>
  
<span data-ttu-id="e7b2f-113">メッセージの送信をサポートするために、メッセージ ストア プロバイダーはメッセージの送信処理中に、MAPI スプーラーによって使用される他の方法だけでなく、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)メソッドをサポートしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-113">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process.</span></span> <span data-ttu-id="e7b2f-114">メッセージ ストアの送信キューをメッセージ ストアのフォルダー ツリーで任意の場所の実際のフォルダーに対応する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-114">A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree.</span></span> <span data-ttu-id="e7b2f-115">ただし、いずれかを使用する必要がある場合、[送信トレイ] フォルダーで、メッセージの発信キューの内容を表示するのには、メッセージ ストア プロバイダーの慣習です。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-115">However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one.</span></span> <span data-ttu-id="e7b2f-116">クライアント アプリケーションにメッセージ ・ ストア内の他のすべてのフォルダーと、[送信トレイ] フォルダーを表示することができますので、ユーザーに送信すると、メッセージの状態を示すために便利な方法は、これを行います。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-116">Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store.</span></span> <span data-ttu-id="e7b2f-117">詳細については、[メッセージ ストア プロバイダーを使用してメッセージの送信](sending-messages-by-using-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7b2f-117">For more information, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7b2f-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="e7b2f-118">See also</span></span>



<span data-ttu-id="e7b2f-119">[���[���̕ۑ��ꏊ�Ńt�H���_�[��������܂��B](implementing-folders-in-message-stores.md)</span><span class="sxs-lookup"><span data-stu-id="e7b2f-119">[Implementing Folders in Message Stores](implementing-folders-in-message-stores.md)</span></span>

