---
title: テーブル パフォーマンス向上のためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 74ab2cfde01d1aeabee3567b556ece6325ccd003
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590920"
---
# <a name="tips-for-better-table-performance"></a>テーブル パフォーマンス向上のためのヒント
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル操作の多くは時間がかかる可能性があり、進行状況を示す方法はないので、パフォーマンスを向上するために次の手法を使用すると便利です。
  
- **[IMAPITable を作成する : IUnknown 呼](imapitableiunknown.md)び出しを正しい順序で行う**
    
   クライアントとサービス プロバイダーは、さまざまな方法でテーブルを使用できます。 既定の列セットと並べ替え順序を使用して、テーブルを開き、すべての行のデータを取得できます。 または、列セットを変更したり、並べ替え順序を変更したり、テーブルの範囲を絞り込む制限を設定したりして、テーブルの既定のビューを変更できます。 データを取得する前に 1 つ以上の操作を実行するテーブル ユーザーは、次の順序で実行する必要があります。
    
    1. [IMAPITable::SetColumns を使用して列セットを定義します](imapitable-setcolumns.md)。
        
    2. [IMAPITable::Restrict を使用して制限を設定します](imapitable-restrict.md)。
        
    3. [IMAPITable::SortTable を使用して並べ替え順序を定義します](imapitable-sorttable.md)。
    
    この順序でこれらのタスクを実行すると、並べ替える行と列の数が制限され、パフォーマンスが向上します。
    
- **可能であれば、TBL_BATCHフラグを使用して操作を遅延する**
    
    メソッドに TBL BATCH フラグを設定すると、テーブルの実装者は、その 1 つを処理する前に、いくつかの呼び出し \_ を収集できます。 リモート サーバーに対して潜在的に多くの呼び出しを行う代わりに。テーブル実装者は 1 つを作成し、すべての操作を一度に実行できます。 操作の結果は、必要になるまで評価されません。 
    
    たとえば、クライアントが [IMAPITable::Restrict](imapitable-restrict.md) を呼び出して TBL BATCH フラグを設定して制限を指定する場合、クライアントが \_ [IMAPITable::QueryRows](imapitable-queryrows.md) を呼び出してデータを取得するまで、制限を有効にする必要はありません。 これにより、テーブル実装者は 2 つの呼び出しの作業を 1 に結合できます。 TBL BATCH フラグを利用するテーブル ユーザーは、これらの条件下でのエラー処理が複雑になる \_ 可能性があります。 
    
    遅延操作によるエラーの処理は、MAPI DEFERRED_ERRORS フラグが設定されている場合のエラーの処理と似ているため、詳細については \_ [、「DELAYING MAPI Errors」](deferring-mapi-errors.md) を参照してください。 
    
- **一般的に使用されるプロパティのキャッシュを保持する**
    
    テーブルを実装するサービス プロバイダーは、一般的に使用されるオブジェクト プロパティのコピーをキャッシュすることで、ビューの作成にかかる時間を減らします。 これらのプロパティのコピーをメモリに保持すると、ビューを再作成する必要があるごとにオブジェクトから取得する必要が省ける必要があります。
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

