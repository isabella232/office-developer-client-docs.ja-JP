---
title: アドレス帳プロバイダー エントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800924"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>アドレス帳プロバイダー エントリ ポイント関数の実装

  
  
**適用対象**: Outlook 
  
プロバイダーとその他のすべてのプロファイルの一部である場合、クライアント アプリケーションの呼び出し[MAPILogonEx](mapilogonex.md)アドレス帳プロバイダーが含まれているプロファイルを使用してセッションを開始するのには、MAPI を読み込みます。 MAPI は、プロファイルを参照して、プロバイダーのエントリ ポイント関数の名前を学習します。 この関数ではありません、DLL エントリ ポイント関数と同じです。**DllMain**の Win32 のドキュメントでのドキュメントを参照してください。 
  
いくつかのエントリ、mapisvc.inf の構成ファイルにする必要があります、すべてのアドレス帳プロバイダーのプロファイルに含まれているがあります。 次の表は、これらのプロファイル] セクションのエントリと、mapisvc.inf ファイルが含める必要があるかどうかを一覧します。
  
|**プロファイル セクションのエントリ**|**mapisvc.inf の要件**|
|:-----|:-----|
|PR_DISPLAY_NAME =_文字列_ <br/> |省略可能  <br/> |
|PR_PROVIDER_DISPLAY =_文字列_ <br/> |必須  <br/> |
|PR_PROVIDER_DLL_NAME = _DLL のファイル名_ <br/> |必須  <br/> |
|PR_RESOURCE_TYPE =_長_ <br/> |必須  <br/> |
|PR_RESOURCE_FLAGS =_ビットマスク_ <br/> |省略可能  <br/> |
   
プロファイル セクションの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すことによって直接または間接的に MAPISVC.INF を変更することによって、アドレス帳プロバイダーはプロファイルには、この情報を配置できます。 プロファイルは、MAPISVC に関連する情報を使用して構築されます。選択したサービス プロバイダーまたはサービスのメッセージの INF です。 詳細については、組織と MAPISVC の内容です。INF、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。
  
アドレス帳プロバイダーの DLL のエントリ ポイント関数の名前は[ABProviderInit](abproviderinit.md)である必要があり、 **ABProviderInit**のプロトタイプにそれに従う必要があります。 プロバイダーの DLL のエントリ ポイント関数では、次のタスクを実行します。 
  
- サービス プロバイダー インターフェイス (SPI) が MAPI を使用して、アドレス帳プロバイダーを使用しているバージョンと互換性のあるバージョンかどうかを確認するのにはのバージョンを確認してください。
    
- アドレス帳プロバイダー オブジェクトのインスタンスを作成します。
    
**生じます**か、 **MAPIUninitialize**をこの関数に呼び出さないでください。 
  
DLL エントリ ポイント関数では、プロバイダー オブジェクトをインスタンス化し、MAPI にそのオブジェクトへのポインターを返します。 
  

