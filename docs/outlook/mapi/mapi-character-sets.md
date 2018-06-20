---
title: MAPI の文字セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3f94823eb3f90ff9ac0f472a2de64e1904920d9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801337"
---
# <a name="mapi-character-sets"></a>MAPI の文字セット

  
  
**適用されます**: Outlook 
  
MAPI 準拠のクライアント アプリケーションとサービス ・ プロバイダーは、ANSI 文字 (1 バイト)、または Unicode 文字 (2 バイト) を使用できます。 OEM 文字セットはサポートされていません。 OEM 文字列は、MAPI メソッドに渡される、または関数と、そのメソッドまたは関数が失敗します。 OEM 文字セットでファイル名を使用するクライアント アプリケーションは、MAPI のメソッドまたは関数に渡す前に ANSI に変換するのには注意が必要である必要があります。
  
Unicode をサポートしている文字セットは、クライアントとサービス ・ プロバイダーの両方はオプションです。 Unicode をサポートしているかどうかに関係なくコンパイルすることができるように、すべてのサービス プロバイダーでのコードを記述する必要があります。 クライアントは、サポートのレベルに応じて条件付きでコンパイルしますが、サービス プロバイダーがありません。 文字セットが変更されたときに再コンパイルする必要はありません。 サービス プロバイダーのコードには何も条件付きにする必要があります。 
  
クライアント、または Unicode の作成に入力パラメーターまたは出力パラメーターとして文字列を含むメソッドの呼び出しをサポートするサービス ・ プロバイダー、MAPI_UNICODE フラグが設定します。 このフラグを設定することを示します実装は、受信したすべての文字列を Unicode 文字列です。 出力では、このフラグ要求の実装から渡されるすべての文字列のバックアップを設定する必要があります Unicode 文字列可能な場合です。 Unicode をサポートしているメソッドの実装者は、要求に従いますUnicode サポートを提供していないメソッドの実装は準拠していません。 PT_STRING8 の種類は、Unicode 形式ではない文字列プロパティです。
  
MAPI では、ヘッダー ファイル MAPIDEFS に**fMapiUnicode**の定数を定義します。既定の文字セットを表す H をします。 クライアントまたはサービス プロバイダーは、Unicode をサポートする場合は、 **fMapiUnicode**が MAPI_UNICODE に設定されます。 クライアントと Unicode をサポートしていないサービス ・ プロバイダーは、 **fMapiUnicode**を 0 に設定します。 
  
Unicode をサポートしていないサービス ・ プロバイダーは次のとおりです。
  
- 文字セット間で変換を実行することを拒否します。
    
- メソッドの呼び出しで、MAPI_UNICODE フラグを渡すことはありません。
    
- MAPI_E_BAD_CHARWIDTH は、MAPI_UNICODE フラグが渡されたときに返されます。
    
- ANSI 文字列のプロパティを明示的に宣言します。 
    
サービス プロバイダーでは、Unicode およびクライアントのみをサポートするときに MAPI_E_BAD_CHARWIDTH は、MAPI_UNICODE フラグを渡さないようにする必要を返すこともします。 
  
 現在のバージョンの MAPI では、次のメソッドの Unicode をサポートしています。 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)(**IAddrBook**の実装のみ) 
  
これらのメソッドの呼び出し元は、Unicode 文字列であると返される文字列を期待できます。 MAPI の実装の他のメソッドから返される文字列を ANSI 文字の文字列となります。
  

