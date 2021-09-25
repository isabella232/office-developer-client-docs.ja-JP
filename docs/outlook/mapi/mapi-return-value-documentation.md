---
title: MAPI 戻り値のドキュメント
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c746b85716af43ac5a65be62d087822a88d5482
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610196"
---
# <a name="mapi-return-value-documentation"></a>MAPI 戻り値のドキュメント

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このリファレンス ドキュメントの参照エントリは、クライアント アプリケーションによる処理が必要な戻り値のみを示します。 一般的なエラー状態を示す値を返し、エラーの確認によって誘導される可能性がある値は、ドキュメントには含まれません。 たとえば、呼び出し元が入力パラメーターに間違ったMAPI_E_INVALID_PARAMETER指定した場合、多くのインターフェイス メソッドでエラーが返される場合があります。 この値は通常、MAPI_E_INVALID_PARAMETER を特に探す必要はないので、予期される戻り値のセットには表示されません。他のエラーとは異なる方法で処理する必要はありません。 一方、一部のサービス プロバイダーはイベント通知をサポートしていないので **、IMAPISession** を通じてクライアントMAPI_E_NO_SUPPORT **Advise** メソッドに戻ります。 クライアントはこの値を明示的にチェックし、それが発生した場合に表す条件を処理するコードを提供する必要があるため、MAPI_E_NO_SUPPORT は [IMAPISession::Advise](imapisession-advise.md)の戻り値の一覧に含まれています。
  
次の表では、メソッドや関数から一般的に返されるエラー値について説明し、クライアントまたはサービス プロバイダーの部分で明示的な処理を必要とします。 これらの値は、無効な入力データを示す値、リソースの問題を示す値、文字セットの互換性を示す値、不明な発生元のエラーを示す値の 4 つのカテゴリに分類されます。
  
|**戻り値**|**説明**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |メソッドまたは関数に渡された 1 つ以上のパラメーターが無効です。  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |flags パラメーターの 1 つ以上の値が無効です。  <br/> |
|MAPI_E_DISK_ERROR  <br/> |ディスクへの書き込みまたはディスクからの読み取りに問題が発生しました。  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |操作を完了するために使用できるディスク領域が足りなかった。  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |操作を完了するのに十分なメモリが使用できません。  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |操作を完了するのに十分なシステム リソースが使用できません。  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |非互換性は、呼び出し元と実装でサポートされる文字セットに存在します。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |予期しない、または不明な発生源のエラーが発生しました。  <br/> |
   
MAPI 戻り値を表す定数は、MAPICODE に一覧表示されます。H ヘッダー ファイル。 定数の一部は Win32 エラーにマップされます。これらの定数と数値のマッピングは、Win32 ヘッダー ファイル WINERROR.H で確認できます。
  
呼び出し元によって渡された無効なデータに関するエラーは、MAPI によって提供されるパラメーター検証 API 関数または一連のマクロを使用して判断できます。 
  
文字セットの非互換性は、次のいずれかの状況が発生した場合に発生します。
  
- クライアントまたはサービス プロバイダーは、メソッドMAPI_UNICODE呼び出しでこのフラグを設定し、実装は Unicode をサポートしません。 このMAPI_UNICODEは、入力として渡される文字列が Unicode 文字列であり、出力として返される文字列が Unicode 文字列である必要があります。
    
- クライアントまたはサービス プロバイダーは、メソッドまたは関数呼び出しMAPI_UNICODEフラグを設定しません。実装は Unicode のみをサポートします。
    

