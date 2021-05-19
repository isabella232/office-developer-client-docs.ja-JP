---
title: MAPI 文字セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417554"
---
# <a name="mapi-character-sets"></a>MAPI 文字セット

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 準拠のクライアント アプリケーションとサービス プロバイダーは、ANSI 文字 (1 バイト) または Unicode 文字 (2 バイト) を使用できます。 OEM 文字セットはサポートされていません。 MAPI メソッドまたは関数に渡される OEM 文字列によって、そのメソッドまたは関数が失敗します。 OEM 文字セット内のファイル名を処理するクライアント アプリケーションは、MAPI メソッドまたは関数に渡す前に、ANSI に変換する必要があります。
  
Unicode 文字セットのサポートは、クライアントとサービス プロバイダーの両方でオプションです。 すべてのサービス プロバイダーは、Unicode をサポートするかどうかに関係なくコンパイルできるよう、コードを記述する必要があります。 クライアントは、サポートのレベルに応じて条件付きでコンパイルされますが、サービス プロバイダーはコンパイルしません。 文字セットが変更された場合は、再コンパイルする必要があります。 サービス プロバイダー コード内の条件を指定する必要はありません。 
  
Unicode をサポートするクライアントまたはサービス プロバイダーが、文字列を入力パラメーターまたは出力パラメーターとして含むメソッド呼び出しを行う場合は、MAPI_UNICODEフラグを設定します。 このフラグを設定すると、すべての受信文字列が Unicode 文字列である実装が示されます。 出力時に、このフラグを設定すると、実装から返される文字列はすべて、可能であれば Unicode 文字列である必要があります。 Unicode をサポートするメソッド実装者は要求に準拠します。Unicode サポートを提供しないメソッド実装者は準拠しない。 Unicode 形式ではない文字列プロパティは、文字列型PT_STRING8。
  
MAPI は、ヘッダー ファイル MAPIDEFS で **fMapiUnicode** 定数を定義します。既定の文字セットを表す H。 クライアントまたはサービス プロバイダーが Unicode をサポートしている場合 **、fMapiUnicode** はユーザー設定にMAPI_UNICODE。 Unicode をサポートしていないクライアントとサービス プロバイダーは **、fMapiUnicode を 0** に設定します。 
  
Unicode をサポートしていないサービス プロバイダーは、次の操作を行う必要があります。
  
- 文字セット間の変換の実行を拒否します。
    
- メソッド呼び出しでMAPI_UNICODEフラグを渡す必要があります。
    
- フラグMAPI_E_BAD_CHARWIDTH渡されたMAPI_UNICODEを返します。
    
- ANSI 文字列プロパティを明示的に宣言します。 
    
サービス プロバイダーは、Unicode のみをMAPI_E_BAD_CHARWIDTHし、クライアントがコード フラグを渡MAPI_UNICODEできます。 
  
 MAPI の現在のバージョンでは、次のメソッドで Unicode がサポートされています。 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) **(IAddrBook 実装** のみ) 
  
これらのメソッドでは、呼び出し元は、返される文字列が Unicode 文字列である必要があります。 他のメソッドの MAPI 実装から返される文字列は、ANSI 文字文字列になります。
  

