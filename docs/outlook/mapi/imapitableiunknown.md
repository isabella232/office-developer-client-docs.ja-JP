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
  
テーブルの読み取り専用のビューを提供します。 **IMAPITable**は、クライアントとサービスプロバイダーが表の表示方法を操作するために使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |Table オブジェクト  <br/> |
|実装元:  <br/> |サービスプロバイダーと MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーション、サービスプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPITable  <br/> |
|ポインターの種類:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |表の前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[助言](imapitable-advise.md) <br/> |テーブルに影響を与える指定したイベントの通知を受信するように登録します。  <br/> |
|[アドバイズ](imapitable-unadvise.md) <br/> |**IMAPITable:: Advise**メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |テーブルの状態と種類を返します。  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |表に列として表示されるプロパティとプロパティの順序を定義します。  <br/> |
|[querycolumns](imapitable-querycolumns.md) <br/> |テーブルの列のリストを返します。  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |テーブル内の行の総数を返します。  <br/> |
|[seekrow](imapitable-seekrow.md) <br/> |テーブル内の特定の位置にカーソルを移動します。  <br/> |
|[seekrowapprox](imapitable-seekrowapprox.md) <br/> |テーブル内のおおよその分数位置にカーソルを移動します。  <br/> |
|[queryposition](imapitable-queryposition.md) <br/> |小数値に基づいて、カーソルの現在のテーブル行の位置を取得します。  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |特定の検索条件に一致するテーブル内の次の行を検索します。  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |テーブルにフィルターを適用し、指定された条件に一致する行だけを行のセットに絞ります。  <br/> |
|[createbookmark](imapitable-createbookmark.md) <br/> |テーブルの現在の位置を示します。  <br/> |
|[freebookmark](imapitable-freebookmark.md) <br/> |ブックマークに関連付けられているメモリを解放します。  <br/> |
|[sorttable](imapitable-sorttable.md) <br/> |並べ替えの基準に基づいて、テーブルの行の順序を示します。  <br/> |
|[querysortorder](imapitable-querysortorder.md) <br/> |テーブルの現在の並べ替え順序を取得します。  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |現在のカーソル位置から、1つまたは複数の行をテーブルから返します。  <br/> |
|[中止](imapitable-abort.md) <br/> |テーブルに対して現在進行中のすべての非同期操作を停止します。  <br/> |
|[expandrow](imapitable-expandrow.md) <br/> |折りたたまれたテーブルカテゴリを展開し、そのカテゴリに属するリーフ行をテーブルビューに追加します。  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |拡張されたテーブルカテゴリを折りたたみ、テーブルビューからそのカテゴリに属するリーフ行を削除します。  <br/> |
|[waitforcompletion](imapitable-waitforcompletion.md) <br/> |テーブルで進行中の1つ以上の非同期操作が完了するまで処理を中断します。  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |カテゴリ化されたテーブルの現在の折りたたまれた状態または展開された状態を再構築するために必要なデータを返します。  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |以前の**IMAPITable:: GetCollapseState**メソッドの呼び出しによって保存されたデータを使用して、カテゴリ化されたテーブルの現在の展開状態または折りたたみ状態を再構築します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

