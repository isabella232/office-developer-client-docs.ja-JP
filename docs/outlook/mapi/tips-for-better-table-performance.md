---
title: テーブルのパフォーマンスを向上させるためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804107"
---
# <a name="tips-for-better-table-performance"></a>テーブルのパフォーマンスを向上させるためのヒント
  
**適用されます**: Outlook 
  
テーブル操作の多くは時間がかかり、進行状況を示す方法がないため、パフォーマンスを向上させるための次の方法を使用すると便利です。
  
- **作成[IMAPITable: IUnknown](imapitableiunknown.md) 、正しい順序で呼び出す**
    
   クライアントとサービス ・ プロバイダーは、さまざまな方法でテーブルを操作できます。 テーブルを開き、すべての既定の列セットを使用して行のデータを取得し、並べ替え順序をことができます。 代わりに、この既定のビュー、テーブルの列セットを変更する、並べ替え順序を変更する、またはテーブルの範囲を絞り込むには制限を確立することによって変更します。 すべてのデータを取得する前にこれらの操作のいずれかを実行する予定があるテーブル ユーザーは、次の順序でを実行する必要があります。
    
    1. [IMAPITable::SetColumns](imapitable-setcolumns.md)に設定されている列を定義します。
        
    2. [IMAPITable::Restrict](imapitable-restrict.md)の制限を設定します。
        
    3. [IMAPITable::SortTable](imapitable-sorttable.md)での並べ替え順序を定義します。
    
    次の順序でこれらのタスクを実行すると、行と列を並べ替えるとき、それによってパフォーマンスが向上する数が制限されます。
    
- **可能な場合、TBL_BATCH フラグを使用して操作を遅延させる**
    
    テーブルを設定する\_メソッドでのバッチのフラグにより、それらのいずれかのアクションを実行する前にいくつかの呼び出しを収集するためにテーブルの作成者です。 代わりにリモート サーバーへの可能性がある多くの呼び出しを行うテーブルの作成者は作成、すべての操作を同時に実行します。 必要でない限り、操作の結果は評価されません。 
    
    クライアントが、テーブルの制限を指定する[IMAPITable::Restrict](imapitable-restrict.md)を呼び出すと、\_バッチ フラグが設定を有効に、クライアントがデータを取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出すまで、制限は必要はありません。 これにより、2 つの呼び出しを 1 つの作業を結合するテーブルの作成者です。 テーブル、テーブルを利用するユーザー\_バッチのフラグより複雑なエラー条件を処理できることに注意する必要があります。 
    
    エラーの処理に似ていますが、遅延操作からのエラーを処理するために MAPI\_DEFERRED_ERRORS フラグが設定されて、詳細については[保留する MAPI エラー](deferring-mapi-errors.md)を参照してください。 
    
- **一般的に使用されるプロパティのキャッシュを保持します。**
    
    テーブルを実装するサービス プロバイダーは、一般的に使用されるオブジェクトのプロパティのコピーをキャッシュすることによってビューを作成するのにかかる時間を軽減できます。 メモリ保存のたびに、オブジェクトから取得することで、ビューのこれらのプロパティのコピーを保持することは再構築する必要があります。
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

