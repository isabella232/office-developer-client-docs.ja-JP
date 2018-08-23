---
title: MAPI の戻り値のドキュメント
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801449"
---
# <a name="mapi-return-value-documentation"></a>MAPI の戻り値のドキュメント

  
  
**適用対象**: Outlook 
  
この参照の参照のエントリは、クライアント アプリケーションによっていくつかの処理を必要とする戻り値だけを文書化します。 共通のエラー条件を指定してエラーを確認することで推定できますが、戻り値は、ドキュメントには含まれません。 などの多くのインターフェイスのメソッドは、呼び出し元が入力パラメーターに間違った値を指定した場合、MAPI_E_INVALID_PARAMETER を返すことができます。 この値は通常表示されない予期される戻り値のセットで MAPI_E_INVALID_PARAMETER 用に特別に確認する必要があると、他のエラーから異なる方法で処理する必要はありませんがないためです。 その一方で、サービス プロバイダーによってはイベント通知をサポートしていないと、 **IMAPISession**によって、クライアントが**アドバイズ**メソッドに MAPI_E_NO_SUPPORT を返します。 クライアントは、明示的にこの値をチェックし、その条件を処理するためのコードにする必要がありますを提供する必要があるために発生する、MAPI_E_NO_SUPPORT は[IMAPISession::Advise](imapisession-advise.md)の戻り値の一覧に含まれています。
  
次の表では、メソッドおよび関数から返される通常し、クライアントまたはサービス プロバイダー側で明示的な処理を必要とするエラー値について説明します。 これらの値は次の 4 つのカテゴリに分類されます: 無効な入力データを示す値、リソースの問題を示す、文字セットの非互換性を示す値と値を原因不明のエラーを示しています。
  
|**戻り値**|**説明**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |1 つ以上のパラメーターがメソッドに渡される、または機能が無効であった。  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Flags パラメーターの 1 つまたは複数の値が無効でした。  <br/> |
|MAPI_E_DISK_ERROR  <br/> |書き込みまたはディスクからの読み取りに問題が発生しました。  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |十分なディスク領域は、操作を完了できませんでした。  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |十分なメモリ操作を完了できませんでした。  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |十分なシステム リソースは、操作を完了できませんでした。  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |互換性の問題は、呼び出し元との実装でサポートされている文字セットに存在します。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |予期しない、または不明な発生元のエラーが発生しました。  <br/> |
   
MAPICODE は、MAPI の戻り値を表す定数の一覧です。H ヘッダー ファイルです。 マップ クラスの定数の Win32 エラーです。数値を指定するこれらの定数へのマッピングは、Win32 ヘッダー ファイル、WINERROR を参照しています。H.
  
パラメーター検証 API 関数のいずれか MAPI またはマクロのセットによって提供される、呼び出し元によって渡される、無効なデータに関するエラーを確認できます。 
  
文字セットの非互換性が発生した次のいずれかが発生したとき。
  
- クライアントまたはサービス プロバイダーは、メソッドまたは関数の呼び出しに MAPI_UNICODE フラグを設定し、実装は Unicode をサポートしていません。 設定 MAPI_UNICODE は、入力として渡される文字列が Unicode 文字列と、出力として渡される文字列が Unicode 文字列であると予測されることを示します。
    
- クライアントまたはサービス プロバイダーはメソッドまたは関数の呼び出しに MAPI_UNICODE フラグを設定しないと、実装には、Unicode のみサポートしています。
    

