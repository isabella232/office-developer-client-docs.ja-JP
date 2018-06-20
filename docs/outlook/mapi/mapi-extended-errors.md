---
title: MAPI �g���G���[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0a9fc55-f4ab-45d8-98cc-b040f9ef6aa4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38e9418d5d9559b67bd79536635359ffaa3f724d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801345"
---
# <a name="mapi-extended-errors"></a>MAPI �g���G���[

  
  
**適用されます**: Outlook 
  
(S_OK) の成功と失敗 (MAPI_E_CALL_FAILED) を単に返すか、エラー条件、状況に適した、多くのエラー値を返すことの間で区別するためにインターフェイス メソッドの実装を選択できます。 ほとんどの場合に、MAPICODE では、MAPI によって定義されているエラー値のいずれかを使用できます。H ヘッダー ファイルです。 ただし、状況のことは説明しませんで定義済みの値、値の MAPI_E_EXTENDED_ERROR を使用することができます。 MAPI_E_EXTENDED_ERROR は、呼び出し元に、エラーに関する詳細情報があることを示します。 呼び出し元は、MAPI_E_EXTENDED_ERROR が返されますが同じオブジェクトを**返します**メソッドを呼び出して、追加情報を取得します。 
  
 MAPI_E_EXTENDED_ERROR だけでなく、すべてのエラー コードに関する情報を取得するのには、 **GetLastError**を呼び出すことができます。 MAPI オブジェクトの多くは、 **GetLastError**メソッドを含むインターフェイスを実装します。 **GetLastError**を含んだ、理論的には、連結前のメソッドの呼び出しによって生成されたすべてのエラーの 1 つ**MAPIERROR**構造体を返します。 詳細については、 [MAPIERROR](mapierror.md)を参照してください。 、呼び出し元としては、オブジェクトの実装側が提供することを必須ではありませんのでこの追加のエラー情報を利用することに依存することをお勧めします。 ただし、実装者は、MAPI_E_EXTENDED_ERROR を返すときにできるため、エラーに関する有用な情報を含む**MAPIERROR**構造体を取得する呼び出し元を強くお勧めします。 
  
**GetLastError**は Windows SDK の一部である API 関数でもあるので、忘れ、MAPI の**GetLastError**インターフェイス メソッドでは、MAPI オブジェクトにのみと呼ばれることができますができます。 別の簡単なミス、不適切なオブジェクトに**GetLastError**を呼び出しています。 エラーを生成したオブジェクトには、 **GetLastError**を呼び出す必要があります。 などを呼び出すと、セッションで、クライアントは、MAPI 処理のためには、サービス プロバイダーへの呼び出しを転送する場合は、クライアント呼び出さないでください。 **GetLastError**サービス プロバイダー オブジェクト。 **IMAPISession::GetLastError**は、適切な呼び出しです。セッション オブジェクトの**GetLastError**を呼び出す必要があります。 詳細については、 [IMAPISession::GetLastError](imapisession-getlasterror.md)を参照してください。
  

