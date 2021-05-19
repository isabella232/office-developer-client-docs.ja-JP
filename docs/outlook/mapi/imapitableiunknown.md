---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420116"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの読み取り専用ビューを提供します。 **IMAPITable は** 、クライアントとサービス プロバイダーがテーブルの表示方法を操作するために使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |Table オブジェクト  <br/> |
|実装元:  <br/> |サービス プロバイダーと MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション、サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPITable  <br/> |
|ポインターの種類:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |テーブルの前 [のエラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。  <br/> |
|[アドバイス](imapitable-advise.md) <br/> |テーブルに影響を与える指定されたイベントの通知を受信するために登録します。  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |**IMAPITable::Advise** メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |テーブルの状態と型を返します。  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |テーブルに列として表示するプロパティの特定のプロパティと順序を定義します。  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |テーブルの列の一覧を返します。  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |テーブル内の行の総数を返します。  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |テーブル内の特定の位置にカーソルを移動します。  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |カーソルをテーブル内のおおよその小数位置に移動します。  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |小数部の値に基づいて、カーソルの現在のテーブル行の位置を取得します。  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |特定の検索条件に一致するテーブル内の次の行を検索します。  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |テーブルにフィルターを適用し、指定した条件に一致する行にのみ行セットを減らします。  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |テーブルの現在の位置をマークします。  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |ブックマークに関連付けられているメモリを解放します。  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |並べ替え条件に基づいてテーブルの行を並べ替える。  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |テーブルの現在の並べ替え順序を取得します。  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |現在のカーソル位置から始まる、テーブルから 1 つ以上の行を返します。  <br/> |
|[中止](imapitable-abort.md) <br/> |テーブルの現在進行中の非同期操作を停止します。  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフ行をテーブル ビューに追加します。  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |展開されたテーブル カテゴリを折りたたみ、そのカテゴリに属するリーフ行をテーブル ビューから削除します。  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |テーブルで進行中の 1 つ以上の非同期操作が完了するまで、処理を中断します。  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |分類されたテーブルの現在の折りたたみ状態または展開状態を再構築するために必要なデータを返します。  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |**IMAPITable::GetCollapseState** メソッドの以前の呼び出しによって保存されたデータを使用して、分類されたテーブルの現在の展開状態または折りたたみ状態を再構築します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

