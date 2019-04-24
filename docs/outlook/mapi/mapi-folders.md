---
title: MAPI �t�H���_�[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6c00dce9ec489ca2b886f3e51551ba57e9eeea33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331564"
---
# <a name="mapi-folders"></a><span data-ttu-id="872e6-103">MAPI �t�H���_�[</span><span class="sxs-lookup"><span data-stu-id="872e6-103">MAPI Folders</span></span>

  
  
<span data-ttu-id="872e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="872e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="872e6-p101">Folders are MAPI objects that serve as the basic unit of organization for messages. Arranged hierarchically, folders can contain messages and other folders. Folders make it easier to locate and work with messages.</span><span class="sxs-lookup"><span data-stu-id="872e6-p101">Folders are MAPI objects that serve as the basic unit of organization for messages. Arranged hierarchically, folders can contain messages and other folders. Folders make it easier to locate and work with messages.</span></span>
  
<span data-ttu-id="872e6-p102">Folders implement the [IMAPIFolder](imapifolderimapicontainer.md) interface, which indirectly inherits from the **IUnknown** interface through the [IMAPIContainer](imapicontainerimapiprop.md) and [IMAPIProp](imapipropiunknown.md) interfaces. Clients use **IMAPIFolder** to create, copy, and delete messages and folders, to retrieve and set message status, and to set or clear the read flag for a message. Although message store providers are required to support all the methods in **IMAPIFolder**, some methods introduce a level of complexity that message store providers might want to avoid. MAPI saves message store providers some work by implementing some of the more complex folder functionality in the [IMAPISupport](imapisupportiunknown.md) interface. Rather than implementing their own copy methods, for example, message store providers can call the copy methods in the support object and get the same results.</span><span class="sxs-lookup"><span data-stu-id="872e6-p102">Folders implement the [IMAPIFolder](imapifolderimapicontainer.md) interface, which indirectly inherits from the **IUnknown** interface through the [IMAPIContainer](imapicontainerimapiprop.md) and [IMAPIProp](imapipropiunknown.md) interfaces. Clients use **IMAPIFolder** to create, copy, and delete messages and folders, to retrieve and set message status, and to set or clear the read flag for a message. Although message store providers are required to support all the methods in **IMAPIFolder**, some methods introduce a level of complexity that message store providers might want to avoid. MAPI saves message store providers some work by implementing some of the more complex folder functionality in the [IMAPISupport](imapisupportiunknown.md) interface. Rather than implementing their own copy methods, for example, message store providers can call the copy methods in the support object and get the same results.</span></span> 
  
<span data-ttu-id="872e6-113">�t�H���_�[�� 3 ��ނ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="872e6-113">There are three kinds of folders:</span></span>
  
- <span data-ttu-id="872e6-114">���[�g �t�H���_�[�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="872e6-114">Root folders.</span></span>
    
- <span data-ttu-id="872e6-115">�ėp�t�H���_�[�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="872e6-115">Generic folders.</span></span>
    
- <span data-ttu-id="872e6-116">�t�H���_�[��������܂��B</span><span class="sxs-lookup"><span data-stu-id="872e6-116">Search folders.</span></span>
    
<span data-ttu-id="872e6-p103">Every message store has at least a root folder. The root folder appears at the top of the hierarchy and contains messages and other folders. Root folders cannot be moved, copied, renamed, or deleted. There is only one root folder for each message store.</span><span class="sxs-lookup"><span data-stu-id="872e6-p103">Every message store has at least a root folder. The root folder appears at the top of the hierarchy and contains messages and other folders. Root folders cannot be moved, copied, renamed, or deleted. There is only one root folder for each message store.</span></span>
  
<span data-ttu-id="872e6-p104">Most other folders are generic folders. Like root folders, generic folders contain messages and other folders. Unlike root folders, they can be moved, copied, renamed, and deleted. Generic folders can be created in the root folder or other generic folders. When a client creates a generic folder in another folder, the new folder is called a subfolder, or child folder. The folder in which the new folder is placed is referred to as the parent folder of the new folder. Generic folders that have the same parent folder are called sibling folders. Both sibling and non-sibling folders may or may not have unique names, depending on the message store provider. Message store providers that require sibling folders to have unique names return the error value MAPI_E_COLLISION when a client attempts to create two folders with the same name in the same parent.</span><span class="sxs-lookup"><span data-stu-id="872e6-p104">Most other folders are generic folders. Like root folders, generic folders contain messages and other folders. Unlike root folders, they can be moved, copied, renamed, and deleted. Generic folders can be created in the root folder or other generic folders. When a client creates a generic folder in another folder, the new folder is called a subfolder, or child folder. The folder in which the new folder is placed is referred to as the parent folder of the new folder. Generic folders that have the same parent folder are called sibling folders. Both sibling and non-sibling folders may or may not have unique names, depending on the message store provider. Message store providers that require sibling folders to have unique names return the error value MAPI_E_COLLISION when a client attempts to create two folders with the same name in the same parent.</span></span> 
  
<span data-ttu-id="872e6-p105">A search folder contains links to messages that match a set of predefined criteria. Because search folders contain links rather than actual messages, they are in effect read-only. They cannot contain other folders or have messages or folders moved or copied into them. They cannot have new messages created in them; and they themselves cannot be moved, copied, or renamed. When a message is deleted from a search folder, it is actually deleted from the folder that contains the message.</span><span class="sxs-lookup"><span data-stu-id="872e6-p105">A search folder contains links to messages that match a set of predefined criteria. Because search folders contain links rather than actual messages, they are in effect read-only. They cannot contain other folders or have messages or folders moved or copied into them. They cannot have new messages created in them; and they themselves cannot be moved, copied, or renamed. When a message is deleted from a search folder, it is actually deleted from the folder that contains the message.</span></span>
  
<span data-ttu-id="872e6-135">フォルダーの種類は、 **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="872e6-135">Folder type is stored in the **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)) property.</span></span> <span data-ttu-id="872e6-136">すべてのフォルダーの種類に応じて、このプロパティは FOLDER_GENERIC、FOLDER_ROOT、または FOLDER_SEARCH のいずれかに設定されています。</span><span class="sxs-lookup"><span data-stu-id="872e6-136">Every folder has this property set to either FOLDER_GENERIC, FOLDER_ROOT, or FOLDER_SEARCH, depending on its type.</span></span>
  
<span data-ttu-id="872e6-137">すべてのフォルダーには、1つのエントリ id と1つのレコードキーがあります。</span><span class="sxs-lookup"><span data-stu-id="872e6-137">Every folder has one entry identifier and one record key.</span></span> <span data-ttu-id="872e6-138">エントリ id **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、クライアントとサービスプロバイダーがフォルダーを開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="872e6-138">The entry identifier, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), is used by clients and service providers to open the folder.</span></span> <span data-ttu-id="872e6-139">record キー **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) は、フォルダーと他のフォルダーを比較するために使用されるバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="872e6-139">The record key, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), is a binary value that is used to compare the folder with other folders.</span></span> 
  
<span data-ttu-id="872e6-140">フォルダーには、関連するフォルダーとメッセージストアを識別するためのその他のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="872e6-140">A folder has other properties to identify related folders and the message store.</span></span> <span data-ttu-id="872e6-141">次のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="872e6-141">The following properties are required:</span></span>
  
- <span data-ttu-id="872e6-142">**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="872e6-142">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="872e6-143">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="872e6-143">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="872e6-144">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="872e6-144">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>
    
<span data-ttu-id="872e6-145">一部のフォルダーは、ユーザーが実行できる操作の種類を示す**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="872e6-145">Some folders support the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property which describes the type of operations a user can perform.</span></span> <span data-ttu-id="872e6-146">たとえば、 **PR_ACCESS**の有効な設定の1つは MAPI_ACCESS_DELETE で、これはフォルダーを削除できることを示します。</span><span class="sxs-lookup"><span data-stu-id="872e6-146">For example, one of the valid settings for **PR_ACCESS** is MAPI_ACCESS_DELETE, which indicates that the folder can be removed.</span></span> <span data-ttu-id="872e6-147">もう1つの設定 MAPI_ACCESS_MODIFY は、フォルダーが変更可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="872e6-147">Another setting, MAPI_ACCESS_MODIFY, indicates that the folder should be modifiable.</span></span> 
  
<span data-ttu-id="872e6-148">必要なフォルダープロパティの完全な一覧については、 [imapifolder](imapifolderimapicontainer.md)インターフェイスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="872e6-148">For a complete list of required folder properties, see the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="872e6-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="872e6-149">See also</span></span>



[<span data-ttu-id="872e6-150">MAPI アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="872e6-150">MAPI Application Development</span></span>](mapi-application-development.md)

