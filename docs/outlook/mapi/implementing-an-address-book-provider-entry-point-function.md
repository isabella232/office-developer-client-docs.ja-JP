---
title: アドレス帳プロバイダーエントリポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332803"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>アドレス帳プロバイダーエントリポイント関数の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションが[MAPILogonEx](mapilogonex.md)を呼び出して、アドレス帳プロバイダーを含むプロファイルを使用してセッションを開始すると、MAPI はプロバイダーとプロファイルの一部である他のすべてを読み込みます。 プロファイルを調べることによって、プロバイダーのエントリポイント関数の名前を MAPI が学習する。 この関数は DLL エントリポイント関数と同じではないことに注意してください。Win32 のドキュメントの**** ドキュメントを参照してください。 
  
mapisvc.inf 構成ファイルにはいくつかのエントリがあり、すべてのアドレス帳プロバイダーのプロファイルセクションに含まれていなければなりません。 次の表に、これらのプロファイルセクションエントリと、mapisvc.inf ファイルにそれらを含める必要があるかどうかを示します。
  
|**プロファイルセクションエントリ**|**mapisvc.inf の要件**|
|:-----|:-----|
|PR_DISPLAY_NAME =_文字列_ <br/> |省略可能  <br/> |
|PR_PROVIDER_DISPLAY =_文字列_ <br/> |必須  <br/> |
|PR_PROVIDER_DLL_NAME = _DLL ファイル名_ <br/> |必須  <br/> |
|PR_RESOURCE_TYPE = _long_ <br/> |必須  <br/> |
|PR_RESOURCE_FLAGS =_ビットマスク_ <br/> |省略可能  <br/> |
   
アドレス帳プロバイダーは、プロファイルセクションの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すか、mapisvc.inf を変更することによって、プロファイルにこの情報を直接配置できます。 プロファイルは、mapisvc.inf の関連情報を使用して作成されます。選択されたサービスプロバイダーまたはメッセージサービスの INF。 mapisvc.inf の組織と内容の詳細については、を参照してください。inf については、「 [File Format of mapisvc.inf](file-format-of-mapisvc-inf.md)」を参照してください。
  
アドレス帳プロバイダーの DLL エントリポイント関数の名前は、 [abproviderinit](abproviderinit.md)である必要があり、 **abproviderinit**プロトタイプに準拠している必要があります。 プロバイダーの DLL エントリポイント関数で次のタスクを実行します。 
  
- サービスプロバイダインターフェイス (SPI) のバージョンを調べて、MAPI が、アドレス帳プロバイダーが使用しているバージョンと互換性のあるバージョンを使用していることを確認します。
    
- アドレス帳プロバイダーオブジェクトをインスタンス化します。
    
この関数で**MAPIInitialize**または**MAPIUninitialize**のいずれかを呼び出すことはできません。 
  
DLL エントリポイント関数は、プロバイダーオブジェクトをインスタンス化し、そのオブジェクトへのポインターを MAPI に返します。 
  

