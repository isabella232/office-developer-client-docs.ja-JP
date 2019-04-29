---
title: 名前解決の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434705"
---
# <a name="implementing-name-resolution"></a>名前解決の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、名前解決のサポートを担当します。これには、エントリ識別子と表示名を関連付けるプロセスがあります。 クライアントは、 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)を呼び出して名前解決を開始し、送信メッセージの受信者リストの各メンバーが有効なアドレスに対応するようにします。 
  
プロバイダーは、次の方法で名前解決をサポートできます。
  
- **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限のサポート (すべてのアドレス帳コンテナーの要件)。
    
- すべてのアドレス帳コンテナーのオプションである[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを実装します。 
    
**IABContainer:: ResolveNames**をサポートすることを選択した場合は、 _lpadrlist_パラメーターを使用して渡された[adrlist](adrlist.md)構造で、未解決の表示名ごとに正確に一致するものを検索します。 未解決の表示名を identifiy することができるのは、 **adrlist**構造の**aentries**メンバーの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティがプロパティ値の配列に含まれていないためです。 0個のプロパティが関連付けられているエントリは無視されます。 
  
_lpflaglist_パラメーターの解決結果を報告します。 _lpadrlist_内の表示名の配列に対応するフラグの配列です。 このフラグは、最初のフラグが**adrlist**構造の最初の**aentries**メンバーに対応するように位置指定し、2番目のフラグは2番目の**aentries**メンバーに対応します。 
  
未解決の各エントリに対して、次の3つの結果が考えられます。
  
- 一致が見つかりませんでした。これは、コンテナーエントリ内のエントリが**adrlist**構造体のエントリと一致しないことを意味します。 _lpflaglist_パラメーターの対応するエントリを MAPI_UNRESOLVED に設定します。 
    
- 複数の一致がある場合は、 **adrlist**構造のエントリに一致する複数のコンテナーエントリがあることを意味します。 _lpflaglist_パラメーターの対応するエントリを MAPI_AMBIGUOUS に設定します。 **adrlist**構造体のエントリの数を変更しないでください。 
    
- 完全一致を見つけることができます。つまり、 **adrlist**構造体のエントリに一致するコンテナーエントリが1つだけであることを意味します。 _lpflaglist_パラメーターの対応するメンバを MAPI_RESOLVED に設定し、 **adrlist**エントリに関連付けられているプロパティの配列にエントリ識別子を追加します。 
    
**IABContainer:: ResolveNames**をサポートしない場合は、実装から MAPI_E_NO_SUPPORT を返します。
  
あいまいな名前解決 ( **PR_ANR**プロパティ制限) をコンテナーのコンテンツテーブルに対してサポートするには、すべてのアドレス帳プロバイダーが必要です。 このサポートを提供するには、お客様のプロバイダーにとって意味のある1つ以上のプロパティと照合して、"最適な推測" の検索を実行して、 [IMAPITable:: Restrict](imapitable-restrict.md)の実装で PR_ANR 制限を処理します。 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) など、同じプロパティまたはプロパティを毎回使用したり、管理者が受け入れ可能なプロパティの一覧から選択できるようにしたりすることができます。 
  
ほとんどのプロバイダーは、独自のコンテンツテーブル実装を提供していますが、 [CreateTable](createtable.md)関数を使用して MAPI で提供される実装をカスタマイズできます。 ただし、MAPI 実装はあらゆる種類の制限をサポートしていないため、ラッパーオブジェクトを作成して、呼び出しをインターセプトするカスタマイズされたバージョンの**制限**を含める必要があります。 
  

