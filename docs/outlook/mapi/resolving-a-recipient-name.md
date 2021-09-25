---
title: 受信者名の解決
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f0e1572c3d02707cc50d2e3f9f4747339ad93f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624350"
---
# <a name="resolving-a-recipient-name"></a>受信者名の解決

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージがアドレス指定された場合、受信者リストは、各受信者に関連するプロパティで構築されます。 メッセージが送信される時には、それらのプロパティの 1 つが受信者の長期エントリ識別子である必要があります。 各受信者に **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれるか確認するには [、IAddrBook::ResolveName](iaddrbook-resolvename.md)の呼び出しで _lpAdrList_ パラメーターの内容の受信者リストを説明する [ADRLIST](adrlist.md)構造を渡します。
  
 **ResolveName** は、対応する [ADRENTRY](adrentry.md)構造体の **SPropValue** 配列にエントリ識別子が存在することで示されている、既に解決されている **ADRLIST** 構造体のエントリを無視して処理を開始します。 次に **、ResolveName は** 2 種類の受信者に 1 回のエントリ識別子を自動的に割り当てる。 
  
- アドレスがインターネット アドレスとして書式設定されている受信者
    
- 次のように書式設定されたアドレスを持つ受信者。
    
     `displayname[address type:email address]`
    
残りのすべてのエントリについて **、ResolveName** はアドレス帳を検索して、表示名と完全に一致します。 **ResolveName** は **、PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティを使用して、検索するコンテナーのセットと検索順序を決定します。 MAPI は、 [すべてのコンテナーの IABContainer::ResolveNames](iabcontainer-resolvenames.md) メソッドを呼び出して、すべての名前を解決します。 一部のコンテナーは **ResolveNames** をサポートしないので、コンテナーが MAPI_E_NO_SUPPORT を返す場合、MAPI はコンテンツ テーブルに対して **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を適用します。 この制限付き名前解決をサポートするには、すべてのアドレス帳コンテナーが必要です。 すべての名前が解決された後、それ以上コンテナー呼び出しは行なされません。 すべてのコンテナーが呼び出されたが、あいまいな名前または未解決の名前が残っている場合、MAPI は、可能であれば、残りの名前を解決するようにユーザーに求めるダイアログ ボックスを表示します。
  
この **PR_ANR** は、ADRLIST 構造の表示 **名** PR_ANRプロパティの値 **と一致** します。 **PR_ANR** プロパティ制限を使用してコンテナーのコンテンツ テーブルのビューを制限すると、アドレス帳プロバイダーは"最適な推測" 型の検索を実行し、プロバイダーに意味のあるプロパティと一致します。 たとえば、あるアドレス帳プロバイダーは、受信者リスト内の名前を **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) と常に一致し、もう 1 つは管理者がプロパティを選択できる場合があります。
  
 **アドレス帳コンテナー PR_ANRのコンテンツ テーブルのプロパティ制限を設定するには**
  
1. 次の [コードに示すように、SRestriction](srestriction.md) 構造を作成します。 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. コンテンツ テーブルの [IMAPITable::Restrict](imapitable-restrict.md) メソッドを呼び出し **、sRestriction** 構造体を  _lpRestriction パラメーターとして渡_ します。 
    

