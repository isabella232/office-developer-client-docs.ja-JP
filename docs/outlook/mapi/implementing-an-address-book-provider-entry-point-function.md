---
title: アドレス帳プロバイダーエントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409714"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>アドレス帳プロバイダーエントリ ポイント関数の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションが [MAPILogonEx](mapilogonex.md) を呼び出して、アドレス帳プロバイダーを含むプロファイルを使用してセッションを開始すると、MAPI はプロバイダーとプロファイルの一部である他のすべてのユーザーを読み込む。 MAPI は、プロファイルを見て、プロバイダーのエントリ ポイント関数の名前を学習します。 この関数は DLL エントリ ポイント関数と同じではありません。Win32 のドキュメント **の DllMain** のドキュメントを参照してください。 
  
mapisvc.inf 構成ファイルに表示する必要があるエントリは、いくつかのエントリで、すべてのアドレス帳プロバイダーのプロファイル セクションに含まれています。 次の表に、これらのプロファイル セクション エントリと、mapisvc.inf ファイルに含める必要があるかどうかを示します。
  
|**プロファイル セクションのエントリ**|**mapisvc.inf の要件**|
|:-----|:-----|
|PR_DISPLAY_NAME= _string_ <br/> |省略可能  <br/> |
|PR_PROVIDER_DISPLAY= _string_ <br/> |必須  <br/> |
|PR_PROVIDER_DLL_NAME= _DLL ファイル名_ <br/> |必須  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |必須  <br/> |
|PR_RESOURCE_FLAGS= _ビットマスク_ <br/> |省略可能  <br/> |
   
アドレス帳プロバイダーは、プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出すことによって、または MAPISVC.INF を変更することで間接的に、この情報をプロファイルに直接配置できます。 プロファイルは、MAPISVC の関連情報を使用して構築されます。選択したサービス プロバイダーまたはメッセージ サービスの INF。 MAPISVC の組織とコンテンツの詳細については、次の情報を参照してください。 [INF、MapiSvc.inf のファイル形式を参照してください](file-format-of-mapisvc-inf.md)。
  
アドレス帳プロバイダーの DLL エントリ ポイント関数の名前は [ABProviderInit](abproviderinit.md) で **、ABProviderInit** プロトタイプに準拠している必要があります。 プロバイダーの DLL エントリ ポイント関数で次のタスクを実行します。 
  
- サービス プロバイダー インターフェイス (SPI) のバージョンを確認して、MAPI がアドレス帳プロバイダーが使用しているバージョンと互換性のあるバージョンを使用している必要があります。
    
- アドレス帳プロバイダー オブジェクトをインスタンス化します。
    
この関数では **、MAPIInitialize または** **MAPIUninitialize を呼** び出さません。 
  
DLL エントリ ポイント関数は、プロバイダー オブジェクトをインスタンス化し、そのオブジェクトへのポインターを MAPI に返します。 
  

