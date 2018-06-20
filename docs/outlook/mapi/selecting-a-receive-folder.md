---
title: 選択すると、フォルダーが表示されます。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803845"
---
# <a name="selecting-a-receive-folder"></a>選択すると、フォルダーが表示されます。

  
  
**適用されます**: Outlook 
  
受信フォルダーは、特定クラスの着信メッセージを配置する場所です。 IPM と関連するレポート メッセージは、MAPI では、既定のフォルダーを受信するように、[受信トレイ] が割り当てられます。 IPC および関連するレポート メッセージは、MAPI では、既定のフォルダーを受信するようにメッセージ ・ ストアのルート フォルダーが割り当てられます。 これらの割り当てを変更したり、他のメッセージ クラスの追加の割り当てを確認できます。 行う明示的な受信フォルダーの割り当て、クライアントでサポートされているクラスは、省略可能なメッセージです。
  
受信のメッセージ クラスは、割り当てられている受信フォルダーを持たない場合、メッセージ ストア プロバイダーは自動的に着信クラスの使用可能な最長のプレフィックスと一致するクラスの受信フォルダーを使用します。 たとえば、次のように、クライアントにはメッセージ クラス IPM の場合です。Note.MyDocument とのみが表示される確立されているフォルダーが IPM メッセージの受信トレイで、このメッセージは、受信トレイにあるため IPM。Note.MyDocument は、IPM の基本クラスから派生します。
  
IPC メッセージの受信フォルダーを割り当てる際は、IPM サブツリーからフォルダーを使用しないでください。 IPM メッセージのみ、これらのフォルダーを予約する必要があります。 メッセージ ストアのルート フォルダー内に含まれているフォルダーを使用します。 
  
 **IPM メッセージ クラスの受信フォルダーを作成するには**
  
1. **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
    
2. 開く IPM サブツリーのルート フォルダーにメッセージ ・ ストア内のエントリの識別子としては、 **PR_IPM_SUBTREE_ENTRYID**と[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
3. 受信フォルダーを作成するのには[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を呼び出します。 
    
4. IPM メッセージ クラスに新しいフォルダーをマップするのには[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出します。 
    
 **IPC メッセージ クラスの受信フォルダーを作成するには**
  
1. メッセージ ・ ストアのルート フォルダーを開くに null のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
2. 受信フォルダーを作成するのには[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を呼び出します。 
    
3. IPC メッセージ クラスに新しいフォルダーをマップするのには[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出します。 
    
関連するレポート メッセージ用のメッセージに使用する受信フォルダーを割り当てます。 IPM をクライアントが受信した場合などです。注意のメッセージのいずれかを設定では、将来の IPM のフォルダーが表示されます。注意のメッセージと同じ Report.IPM.Note のメッセージ用のフォルダーが表示されます。
  

