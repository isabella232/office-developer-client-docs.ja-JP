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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339727"
---
# <a name="selecting-a-receive-folder"></a>受信フォルダーの選択

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信フォルダーには、特定のクラスの受信メッセージが配置されます。 IPM および関連するレポートメッセージの場合、MAPI は既定の受信フォルダーとして受信トレイを割り当てます。 IPC および関連するレポートメッセージの場合、MAPI はメッセージストアのルートフォルダーを既定の受信フォルダーとして割り当てます。 その他のメッセージクラスについては、これらの割り当てを変更したり、追加の割り当てを行ったりすることができます。 クライアントでサポートされているメッセージクラスに対して明示的な受信フォルダーの割り当てを行うことはオプションです。
  
受信メッセージクラスに、受信フォルダーが割り当てられていない場合、メッセージストアプロバイダーは、受信クラスの可能な最大プレフィックスに一致するクラスの受信フォルダーを自動的に使用します。 たとえば、クライアントがクラス IPM というメッセージを受信するとします。メモ: 設定済みの受信フォルダーのみが、ipm メッセージの受信トレイに配置されます。このメッセージは、ipm.注: MyDocument は基本クラス IPM から派生します。
  
IPC メッセージの受信フォルダーを割り当てる場合は、IPM サブツリーのフォルダーは使用しないでください。 これらのフォルダーは、IPM メッセージ専用に予約されている必要があります。 代わりに、メッセージストアのルートフォルダー内に格納されているフォルダーを使用します。 
  
 **IPM メッセージクラスの受信フォルダーを作成するには**
  
1. メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。 
    
2. [IMsgStore:: openentry](imsgstore-openentry.md)を entry 識別子として**PR_IPM_SUBTREE_ENTRYID**で呼び出し、メッセージストア内の IPM サブツリーのルートフォルダーを開きます。 
    
3. [imapifolder:: CreateFolder](imapifolder-createfolder.md)を呼び出して、受信フォルダーを作成します。 
    
4. [IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPM メッセージクラスにマップします。 
    
 **IPC メッセージクラスの受信フォルダーを作成するには**
  
1. [IMsgStore::](imsgstore-openentry.md) null エントリ識別子を持つ openentry を呼び出して、メッセージストアのルートフォルダーを開きます。 
    
2. [imapifolder:: CreateFolder](imapifolder-createfolder.md)を呼び出して、受信フォルダーを作成します。 
    
3. [IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPC メッセージクラスにマップします。 
    
関連するレポートメッセージのメッセージに使用する受信フォルダーを割り当てます。 たとえば、クライアントが IPM を受信したとします。メッセージを確認し、今後の IPM 用に1つの受信フォルダーをセットアップします。メモメッセージと、今後の報告メッセージの同じ受信フォルダー。
  

