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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800852"
---
# <a name="imapitable--iunknown"></a>IMAPITable: IUnknown

  
  
**適用されます**: Outlook 
  
テーブルの読み取り専用ビューを提供します。 **IMAPITable**は、テーブルの表示方法を操作するクライアントとサービス ・ プロバイダーによって使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |テーブル オブジェクト  <br/> |
|によって実装されます。  <br/> |サービス プロバイダーおよび MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション、サービス ・ プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPITable  <br/> |
|ポインターの型。  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imapitable-getlasterror.md) <br/> |テーブルの前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[アドバイス](imapitable-advise.md) <br/> |テーブルに影響を与えず、指定されたイベントの通知を受け取ることを登録します。  <br/> |
|[アドバイズ中止します。](imapitable-unadvise.md) <br/> |**IMAPITable::Advise**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |テーブルのステータスおよび種類を返します。  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |特定のプロパティと、テーブル内の列として表示するプロパティの順序を定義します。  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |テーブルの列の一覧を返します。  <br/> |
|[な](imapitable-getrowcount.md) <br/> |テーブル内の行の合計数を返します。  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |テーブル内の特定の位置にカーソルを移動します。  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |テーブルのおおよその小数部から成る位置にカーソルを移動します。  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |小数部の値に基づいて、カーソルの現在のテーブルの行位置を取得します。  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |特定の検索条件に一致するテーブル内には、次の行を検索します。  <br/> |
|[制限します。](imapitable-restrict.md) <br/> |指定した条件に一致する行のみに設定した行を減らすこと、テーブルにフィルターを適用します。  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |テーブルの現在の位置をマークします。  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |ブックマークに関連付けられているメモリを解放します。  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |並べ替え条件に基づいて、テーブルの行を順序付けします。  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |テーブルの現在の並べ替え順序を取得します。  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |現在のカーソル位置から開始し、テーブルから 1 つまたは複数の行を返します。  <br/> |
|[中止](imapitable-abort.md) <br/> |テーブルの現在進行中のすべての非同期操作を停止します。  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |テーブル ビューをカテゴリに属しているリーフ行の追加、折りたたまれているテーブルのカテゴリを展開します。  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |テーブル ・ ビューのカテゴリに属するリーフ行を削除する、拡張テーブルのカテゴリを折りたたみます。  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |1 つまたは複数の非同期操作の進行状況でテーブルに完了するまでの処理を中断します。  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |現在を再構築するために必要なデータを返しますは、折りたたむか、カテゴリ別のテーブルの状態を展開します。  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |**IMAPITable::GetCollapseState**メソッドへの前回の呼び出しによって保存されたデータを使用して分類されたテーブルの現在の展開または折りたたみの状態を再構築します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

