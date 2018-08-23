---
title: 名前解決の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 489a5888014fa9299b407ebf91759627427b69bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571389"
---
# <a name="implementing-name-resolution"></a>名前解決の実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳プロバイダーは、名前解決をサポートするため、表示名を持つエントリ識別子を関連付けるプロセスです。 クライアントは、送信メッセージの受信者の一覧の各メンバーが有効なアドレスに対応していることを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)を呼び出すときに名前解決を開始します。 
  
プロバイダーによる名前解決をサポートできます。
  
- **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限、アドレス帳コンテナーのすべての要件をサポートします。
    
- アドレス帳コンテナーのすべてのオプション、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。 
    
**IABContainer::ResolveNames**をサポートするために選択した場合は、 _lpAdrList_パラメーターで渡される[ADRLIST](adrlist.md)構造内の未解決名ごとに正確に一致を検索ましょう。 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、 **aEntries** 、 **ADRLIST**構造体のプロパティ値の配列ではないためには、identifiy に未解決の表示名を作成することができます。 プロパティが関連付けられているすべてのエントリを無視します。 
  
_LpAdrList_での表示名の配列に対応するフラグの配列を_lpFlagList_パラメーターでの解像度で、試行の結果を報告します。 フラグは、最初のフラグは、 **ADRLIST**構造体の最初の**aEntries**メンバーに対応するように位置、2 番目のフラグは、 **aEntries**の 2 番目のメンバーというように対応します。 
  
未解決のエントリごとに次の 3 つの可能な結果があります。
  
- 一致しませんでした、 **ADRLIST**構造体のエントリをコンテナーのエントリのエントリと一致することを意味します。 MAPI_UNRESOLVED に_lpFlagList_パラメーターに対応するエントリを設定します。 
    
- **ADRLIST**構造体のエントリに一致する複数のコンテナーのエントリがあることを意味する、いくつかの項目を確認できます。 MAPI_AMBIGUOUS に_lpFlagList_パラメーターに対応するエントリを設定します。 **ADRLIST**構造体のエントリの数は変更されません。 
    
- **ADRLIST**構造体のエントリに一致するコンテナーを 1 つだけエントリがあることを意味する、厳密な一致を確認できます。 MAPI_RESOLVED に_lpFlagList_パラメーターに対応するメンバーを設定し、 **ADRLIST**エントリに関連付けられているプロパティの配列のエントリの識別子を追加します。 
    
**IABContainer::ResolveNames**をサポートしないように選択した場合は、実装から MAPI_E_NO_SUPPORT を返します。
  
あいまいな名前解決をサポートするために必要なすべてのアドレス帳プロバイダー- **PR_ANR**プロパティの制限-そのコンテナーの内容のテーブルにします。 このサポートを提供するには、最適な推測の一種で、プロバイダーの意味のある 1 つまたは複数の特定プロパティと一致する、検索を実行することによって[IMAPITable::Restrict](imapitable-restrict.md)の実装では、PR_ANR の制限を処理します。 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) や**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) など、毎回同じプロパティまたはプロパティを使用して、許容可能なプロパティの一覧から選択するには管理者の許可を選択できます。 
  
ほとんどのプロバイダーは、独自の内容のテーブルの実装を提供、 [CreateTable](createtable.md)関数を介して、MAPI によって提供される実装をカスタマイズできます。 ただし、MAPI 実装がどのような制限をサポートしていないために、呼び出しをインターセプトする**制限**のカスタマイズ バージョンを含むようにラッパー オブジェクトを作成する必要があります。 
  

