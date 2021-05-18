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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421845"
---
# <a name="mapi-folders"></a>MAPI �t�H���_�[

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Folders are MAPI objects that serve as the basic unit of organization for messages. Arranged hierarchically, folders can contain messages and other folders. Folders make it easier to locate and work with messages.
  
Folders implement the [IMAPIFolder](imapifolderimapicontainer.md) interface, which indirectly inherits from the **IUnknown** interface through the [IMAPIContainer](imapicontainerimapiprop.md) and [IMAPIProp](imapipropiunknown.md) interfaces. Clients use **IMAPIFolder** to create, copy, and delete messages and folders, to retrieve and set message status, and to set or clear the read flag for a message. Although message store providers are required to support all the methods in **IMAPIFolder**, some methods introduce a level of complexity that message store providers might want to avoid. MAPI saves message store providers some work by implementing some of the more complex folder functionality in the [IMAPISupport](imapisupportiunknown.md) interface. Rather than implementing their own copy methods, for example, message store providers can call the copy methods in the support object and get the same results. 
  
�t�H���_�[�� 3 ��ނ�����܂��B
  
- ���[�g �t�H���_�[�ɂ��܂��B
    
- �ėp�t�H���_�[�ɂ��܂��B
    
- �t�H���_�[��������܂��B
    
Every message store has at least a root folder. The root folder appears at the top of the hierarchy and contains messages and other folders. Root folders cannot be moved, copied, renamed, or deleted. There is only one root folder for each message store.
  
Most other folders are generic folders. Like root folders, generic folders contain messages and other folders. Unlike root folders, they can be moved, copied, renamed, and deleted. Generic folders can be created in the root folder or other generic folders. When a client creates a generic folder in another folder, the new folder is called a subfolder, or child folder. The folder in which the new folder is placed is referred to as the parent folder of the new folder. Generic folders that have the same parent folder are called sibling folders. Both sibling and non-sibling folders may or may not have unique names, depending on the message store provider. Message store providers that require sibling folders to have unique names return the error value MAPI_E_COLLISION when a client attempts to create two folders with the same name in the same parent. 
  
A search folder contains links to messages that match a set of predefined criteria. Because search folders contain links rather than actual messages, they are in effect read-only. They cannot contain other folders or have messages or folders moved or copied into them. They cannot have new messages created in them; and they themselves cannot be moved, copied, or renamed. When a message is deleted from a search folder, it is actually deleted from the folder that contains the message.
  
フォルダーの種類は、PR_FOLDER_TYPE **(** [PidTagFolderType](pidtagfoldertype-canonical-property.md)) プロパティに格納されます。 すべてのフォルダーには、種類に応じて、FOLDER_GENERIC、FOLDER_ROOT、FOLDER_SEARCHにこのプロパティが設定されています。
  
すべてのフォルダーには、1 つのエントリ識別子と 1 つのレコード キーがあります。 エントリ識別子 **(PR_ENTRYID** [pidTagEntryId) (PidTagEntryId)](pidtagentryid-canonical-property.md)は、クライアントとサービス プロバイダーがフォルダーを開くのに使用します。 レコード キー **(PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)は、フォルダーを他のフォルダーと比較するために使用されるバイナリ値です。 
  
フォルダーには、関連するフォルダーとメッセージ ストアを識別するためのその他のプロパティがあります。 次のプロパティが必要です。
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
一部のフォルダー **では、PR_ACCESS** 実行できる操作の種類を示すプロパティ [(PidTagAccess)](pidtagaccess-canonical-property.md)プロパティがサポートされています。 たとえば、フォルダーを削除できるPR_ACCESS示MAPI_ACCESS_DELETE有効な設定の 1 つが使用されます。 別の設定MAPI_ACCESS_MODIFY、フォルダーを変更可能にする必要があります。 
  
必要なフォルダー プロパティの完全な一覧については [、「IMAPIFolder インターフェイス」を参照](imapifolderimapicontainer.md) してください。 
  
## <a name="see-also"></a>関連項目



[MAPI アプリケーション開発](mapi-application-development.md)

