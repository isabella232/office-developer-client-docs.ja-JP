---
title: ���b�Z�[�W�̃X�g�A��̃t�H���_�[����J���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e7b479931b6b2b00dd3927133187fe058b4c6e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800019"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="c1f5c-103">���b�Z�[�W�̃X�g�A��̃t�H���_�[����J���܂��B</span><span class="sxs-lookup"><span data-stu-id="c1f5c-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="c1f5c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1f5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1f5c-105">すべてのメッセージ ストア プロバイダーは、クライアント アプリケーションに最上位[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-105">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications.</span></span> <span data-ttu-id="c1f5c-106">最上位のフォルダーは、全体のメッセージ ・ ストアに対応します。メッセージ ・ ストアのコンテンツとしてユーザーに表示されるフォルダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-106">The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store.</span></span> <span data-ttu-id="c1f5c-107">IPC メッセージおよびフォルダーと、フォルダーが表示される既定値としてさらに、最上位のフォルダーが使用多くの場合レポートが送信されるを参照するからです。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-107">In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent.</span></span> <span data-ttu-id="c1f5c-108">メッセージ ストア プロバイダーでは、IPM サブツリーが表示もする必要があります: IPM メッセージを格納するために使用するフォルダーのセット-クライアント アプリケーションにします。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-108">Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="c1f5c-p102">�N���C�A���g �A�v���P�[�V�����ł́A  [cbEntryId](imsgstore-openentry.md)�� _lpEntryId_�p�����[�^�[����ꂼ�� 0 �� NULL [IMsgStore::OpenEntry](imsgstore-openentry.md)���\�b�h��g�p���čŏ�ʂ̃t�H���_�[��J�����Ƃ��ł��܂��B�قƂ�ǂ̏ꍇ�A�������A�N���C�A���g �A�v���P�[�V������J���܂� IPM ���b�Z�[�W���܂܂�Ă���t�H���_�[�̐ݒ�B</span><span class="sxs-lookup"><span data-stu-id="c1f5c-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="c1f5c-111">メッセージ ストアの IPM のフォルダー ツリー内のフォルダーの一覧を取得するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="c1f5c-112">[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)���\�b�h��Ăяo���AMAPI �Z�b�V������g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="c1f5c-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="c1f5c-113">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すには、結果のメッセージ データベースのポインターを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="c1f5c-114">[IMAPIFolder](imsgstore-openentry.md)�|�C���^�[��擾�G���g�����ʎq�����**IMsgStore::OpenEntry**���\�b�h��Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="c1f5c-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="c1f5c-115">�t�H���_�[�̓�e�̃e�[�u����擾����[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)���\�b�h��Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="c1f5c-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="c1f5c-116">最上位のフォルダー内のフォルダーを一覧表示する[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="c1f5c-117">MAPI クライアントでは、他のフォルダーのオブジェクトとメッセージ ・ ストア内のメッセージ オブジェクトにアクセスするのにはこれらのフォルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-117">MAPI clients use these folders to access other folder objects and message objects in the message store.</span></span> <span data-ttu-id="c1f5c-118">**IMAPIFolder**、およびその親インターフェイス[IMAPIContainer](imapicontainerimapiprop.md)には、メッセージ オブジェクトを含むフォルダーを作成し、メッセージを処理するクライアント要求に応答する、メッセージ ストア プロバイダーを実装する必要がありますメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1f5c-118">**IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1f5c-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="c1f5c-119">See also</span></span>



<span data-ttu-id="c1f5c-120">[���[���̕ۑ��ꏊ�Ńt�H���_�[��������܂��B](implementing-folders-in-message-stores.md)</span><span class="sxs-lookup"><span data-stu-id="c1f5c-120">[Implementing Folders in Message Stores](implementing-folders-in-message-stores.md)</span></span>

