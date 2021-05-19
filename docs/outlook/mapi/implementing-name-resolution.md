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
  
アドレス帳プロバイダーは、名前解決をサポートする責任があります。エントリ識別子を表示名に関連付け処理します。 クライアントは [、IAddrBook::ResolveName](iaddrbook-resolvename.md) を呼び出す際に名前解決を開始し、送信メッセージの受信者リストの各メンバーが有効なアドレスに対応します。 
  
プロバイダーは、次の方法で名前解決をサポートできます。
  
- すべてのアドレス **PR_ANR** [(PidTagAnr)](pidtaganr-canonical-property.md)プロパティ制限をサポートします。
    
- すべてのアドレス帳 [コンテナーのオプションである IABContainer::ResolveNames](iabcontainer-resolvenames.md) メソッドを実装します。 
    
**IABContainer::ResolveNames** をサポートする場合は _、lpAdrList_ パラメーターと一緒に渡された [ADRLIST](adrlist.md)構造体の未解決の表示名ごとに完全に一致する位置を探します。 **ADRLIST** 構造体の **aEntries** メンバーのプロパティ値配列に **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが存在しないので、未解決の表示名を特定できます。 関連付けられたプロパティが 0 のエントリは無視します。 
  
_lpFlagList パラメーター (lpAdrList_ の表示名の配列に対応するフラグの配列) で解決を試みる結果 _を報告します_。 フラグは、最初のフラグが **ADRLIST** 構造体の最初の **aEntries** メンバーに対応し、2 番目のフラグが 2 番目の **aEntries** メンバーに対応する位置です。 
  
未解決のエントリごとに、次の 3 つの結果が得られます。
  
- 一致が見つかりませんでした。つまり、コンテナー エントリ内のエントリのいずれも ADRLIST 構造内の **エントリと一致** しません。 _lpFlagList_ パラメーターの対応するエントリを設定して、MAPI_UNRESOLVED。 
    
- いくつかの一致が見つかる可能性があります。つまり **、ADRLIST** 構造内のエントリに一致するコンテナー エントリが複数あります。 _lpFlagList_ パラメーターの対応するエントリを設定して、MAPI_AMBIGUOUS。 **ADRLIST** 構造内のエントリの数を変更しない。 
    
- 完全一致を見つけることができます。つまり **、ADRLIST** 構造内のエントリに一致するコンテナー エントリは 1 つのみです。 _lpFlagList_ パラメーターの対応するメンバーを MAPI_RESOLVED に設定し **、ADRLIST** エントリに関連付けられたプロパティの配列にエントリ識別子を追加します。 
    
**IABContainer::ResolveNames** をサポートしない場合は、実装MAPI_E_NO_SUPPORT返します。
  
すべてのアドレス帳プロバイダーは、コンテナーのコンテンツ テーブルのあいまいな名前解決 (PR_ANR **プロパティ制限** ) をサポートする必要があります。 このサポートを提供するには [、IMAPITable::Restrict](imapitable-restrict.md) の実装で PR_ANR 制限を処理し、プロバイダーに適した 1 つ以上の特定のプロパティと照合して、"最適な推測" 型の検索を実行します。 PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) や **PR_ACCOUNT** ([PidTagAccount)](pidtagaccount-canonical-property.md)など、毎回同じプロパティまたはプロパティを使用するか、管理者が受け入れ可能なプロパティの一覧から選択できます。 
  
ほとんどのプロバイダーは、独自のコンテンツ テーブルの実装を提供しますが [、CreateTable](createtable.md) 関数を使用して MAPI によって提供される実装をカスタマイズできます。 ただし、MAPI 実装はいかなる種類の制限もサポートしていないので、呼び出しを傍受するカスタマイズされたバージョンの **Restrict** を含めるラッパー オブジェクトを作成する必要があります。 
  

