---
title: 受信フォルダーの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428418"
---
# <a name="selecting-a-receive-folder"></a>受信フォルダーの選択

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信フォルダーは、特定のクラスの受信メッセージが配置される場所です。 IPM および関連するレポート メッセージの場合、MAPI は受信トレイを既定の受信フォルダーとして割り当てる。 IPC および関連するレポート メッセージの場合、MAPI はメッセージ ストアのルート フォルダーを既定の受信フォルダーとして割り当てる。 これらの割り当てを変更するか、他のメッセージ クラスに追加の割り当てを行います。 クライアントでサポートされているメッセージ クラスに対して明示的な受信フォルダーの割り当てを行う方法はオプションです。
  
受信メッセージ クラスに受信フォルダーが割り当てられていない場合、メッセージ ストア プロバイダーは、受信クラスの可能な限り長いプレフィックスに一致するクラスの受信フォルダーを自動的に使用します。 たとえば、クライアントがクラス IPM のメッセージを受信した場合です。Note.MyDocument と確立された受信フォルダーは IPM メッセージの受信トレイのみです。このメッセージは IPM のため受信トレイに配置されます。Note.MyDocument は、基本クラス IPM から派生します。
  
IPC メッセージの受信フォルダーを割り当てる場合は、IPM サブツリーのフォルダーを使用しません。 これらのフォルダーは、IPM メッセージ専用に予約する必要があります。 代わりに、メッセージ ストアのルート フォルダー内に含まれるフォルダーを使用します。 
  
 **IPM メッセージ クラスの受信フォルダーを作成するには**
  
1. メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_IPM_SUBTREE_ENTRYID **(** [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。 
    
2. メッセージ ストアで IPM サブ **ツリー** のルート フォルダーを開PR_IPM_SUBTREE_ENTRYID ID として [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
3. [IMAPIFolder::CreateFolder を呼び出して](imapifolder-createfolder.md)受信フォルダーを作成します。 
    
4. [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPM メッセージ クラスにマップします。 
    
 **IPC メッセージ クラスの受信フォルダーを作成するには**
  
1. メッセージ ストアのルート フォルダーを開く場合は、NULL エントリ識別子を使用して [IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出します。 
    
2. [IMAPIFolder::CreateFolder を呼び出して](imapifolder-createfolder.md)受信フォルダーを作成します。 
    
3. [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPC メッセージ クラスにマップします。 
    
関連するレポート メッセージのメッセージに使用する受信フォルダーを割り当てる。 たとえば、クライアントが IPM を受信した場合です。メモ メッセージは、将来の IPM 用に 1 つの受信フォルダーを設定します。メッセージと、将来の Report.IPM.Note メッセージ用の同じ受信フォルダーをメモします。
  

