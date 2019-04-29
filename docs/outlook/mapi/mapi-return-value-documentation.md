---
title: MAPI の戻り値の文書化
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429692"
---
# <a name="mapi-return-value-documentation"></a>MAPI の戻り値の文書化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このリファレンスに記載されている参照エントリは、クライアントアプリケーションによって何らかの処理を必要とする戻り値のみを文書化します。 エラー状態をチェックすることによって検出できる一般的なエラー条件を示す戻り値は、このドキュメントには含まれていません。 たとえば、多くのインターフェイスメソッドは、呼び出し元が入力パラメーターに間違った値を指定した場合に MAPI_E_INVALID_PARAMETER を返すことができます。 この値は、通常、MAPI_E_INVALID_PARAMETER を特定する必要がなく、他のエラーとは異なる方法で処理する必要がないため、予想される戻り値のセットには表示されません。 一方、一部のサービスプロバイダーはイベント通知をサポートしておらず、 **imapisession**を通じてクライアントによって作成された**Advise**メソッドに MAPI_E_NO_SUPPORT を返します。 クライアントは、この値を明示的に確認して、それが表す条件を処理するコードを提供する必要があるため、MAPI_E_NO_SUPPORT は[imapisession:: Advise](imapisession-advise.md)の戻り値の一覧に含まれています。
  
次の表では、メソッドと関数から一般的に返されるエラー値と、クライアントまたはサービスプロバイダーの部分を明示的に処理する必要があることを示します。 これらの値は、無効な入力データを示す値、リソースの問題を示す値、文字セットの非互換性を示す値、および不明な配信が失敗したことを示す値の4つのカテゴリに分類されます。
  
|**戻り値**|**説明**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |メソッドまたは関数に渡された1つ以上のパラメーターが有効ではありませんでした。  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |flags パラメーターの1つ以上の値が無効です。  <br/> |
|MAPI_E_DISK_ERROR  <br/> |ディスクへの書き込み中またはディスクからの読み取り中に問題が発生しました。  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |操作を完了するのに十分なディスク容量がありません。  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |メモリが不足しているため、操作を完了できません。  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |システムリソースが不足しているため、操作を完了できませんでした。  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |呼び出し元と実装でサポートされている文字セットに互換性がありません。  <br/> |
|MAPI_E_CALL_FAILED  <br/> |予期しないまたは不明な送信元のエラーが発生しました。  <br/> |
   
MAPI の戻り値を表す定数は、MAPICODE に示されています。H ヘッダーファイル。 一部の定数は Win32 エラーに対応しています。これらの定数を数値にマッピングする方法については、Win32 ヘッダーファイル winerror.h を参照してください。H.
  
呼び出し元によって渡された無効なデータに関するエラーは、MAPI またはマクロのセットによって提供されるパラメーター検証 API 関数のどちらかによって決定できます。 
  
文字セットの非互換性は、次のいずれかの状況が発生した場合に生じます。
  
- クライアントまたはサービスプロバイダーがメソッドまたは関数呼び出しに MAPI_UNICODE フラグを設定していますが、実装で UNICODE がサポートされていません。 MAPI_UNICODE を設定すると、入力として渡された文字文字列が unicode 文字列であること、および出力として返される文字文字列が unicode 文字列であることが想定されます。
    
- クライアントまたはサービスプロバイダーは、メソッドまたは関数呼び出しに MAPI_UNICODE フラグを設定しません。実装では、UNICODE のみがサポートされています。
    

