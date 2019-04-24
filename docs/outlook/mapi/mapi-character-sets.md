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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319076"
---
# <a name="mapi-character-sets"></a>MAPI 文字セット

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 準拠のクライアントアプリケーションおよびサービスプロバイダーは、ANSI 文字 (1 バイト) または Unicode 文字 (2 バイト) を使用できます。 OEM 文字セットはサポートされていません。 MAPI メソッドまたは関数に渡された OEM 文字列は、メソッドまたは関数が失敗する原因になります。 OEM 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI のメソッドまたは関数に渡す前に、それらのファイルを ANSI に変換するために注意する必要があります。
  
クライアントとサービスプロバイダーの両方で、Unicode 文字セットのサポートはオプションです。 すべてのサービスプロバイダーは、Unicode をサポートしているかどうかに関係なく、コンパイルできるようにコードを記述する必要があります。 クライアントは、サポートのレベルに応じて条件付きでコンパイルされますが、サービスプロバイダーには必要ありません。 文字セットが変更されたときには、それらを再コンパイルする必要はありません。 サービスプロバイダーのコードでは、条件付きにすることはできません。 
  
Unicode をサポートするクライアントまたはサービスプロバイダーが、入力パラメーターまたは出力パラメーターとして文字列を含むメソッド呼び出しを行うと、MAPI_UNICODE フラグが設定されます。 このフラグを設定すると、すべての入力文字列が Unicode 文字列であることが実装に対して示されます。 出力時に、このフラグを設定すると、実装から返されたすべての文字列が、可能であれば Unicode 文字列である必要があることが要求されます。 Unicode をサポートするメソッドの実装は、要求に準拠します。Unicode のサポートを提供していないメソッドの実装は準拠していません。 Unicode 形式ではない文字列プロパティの型は PT_STRING8 です。
  
MAPI は、ヘッダーファイル mapidefs.h で**fMapiUnicode**定数を定義します。H を既定の文字セットを表します。 クライアントまたはサービスプロバイダーが Unicode をサポートしている場合、 **fMapiUnicode**は MAPI_UNICODE に設定されます。 Unicode をサポートしていないクライアントおよびサービスプロバイダーは、 **fMapiUnicode**をゼロに設定します。 
  
Unicode をサポートしていないサービスプロバイダーは次のようになります。
  
- 文字セット間の変換を実行することを拒否します。
    
- MAPI_UNICODE フラグをメソッド呼び出しに渡しません。
    
- MAPI_UNICODE フラグが渡されると、MAPI_E_BAD_CHARWIDTH を返します。
    
- ANSI 文字列プロパティを明示的に宣言します。 
    
また、サービスプロバイダーが Unicode のみをサポートしており、クライアントが MAPI_UNICODE フラグを渡さない場合、MAPI_E_BAD_CHARWIDTH を返すこともできます。 
  
 現在のバージョンの MAPI では、次の方法で Unicode がサポートされています。 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[imapiprop:: GetLastError](imapiprop-getlasterror.md)(**IAddrBook**の実装のみ) 
  
これらのメソッドでは、呼び出し元は、返される文字列を Unicode 文字列として受け取ることができます。 その他のメソッドの MAPI 実装から返される文字列は、ANSI 文字の文字列になります。
  

