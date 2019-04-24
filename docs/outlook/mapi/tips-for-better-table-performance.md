---
title: テーブル パフォーマンス向上のためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327798"
---
# <a name="tips-for-better-table-performance"></a>テーブル パフォーマンス向上のためのヒント
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル操作の多くは時間がかかることがあり、進行状況を示す方法がないため、次の方法を使用してパフォーマンスを向上することをお勧めします。
  
- **[IMAPITable: IUnknown](imapitableiunknown.md)呼び出しを正しい順序で行う**
    
   クライアントとサービスプロバイダーは、さまざまな方法でテーブルを操作できます。 既定の列セットと並べ替え順序を使用して、テーブルを開き、すべての行のデータを取得することができます。 または、列セットを変更したり、並べ替え順序を変更したり、テーブルの範囲を絞るために制限を設定したりすることによって、テーブルの既定のビューを変更することもできます。 テーブルデータを取得する前に、これらの操作を1つ以上実行する予定のユーザーは、次の順序で実行する必要があります。
    
    1. [IMAPITable:: SetColumns](imapitable-setcolumns.md)を使用して、列セットを定義します。
        
    2. [IMAPITable:: Restrict](imapitable-restrict.md)を使用して制限を設定します。
        
    3. [IMAPITable:: sorttable](imapitable-sorttable.md)を使用して、並べ替え順序を定義します。
    
    これらのタスクをこの順序で実行すると、並べ替えられる行と列の数が制限されるため、パフォーマンスが向上します。
    
- **可能であれば、TBL_BATCH フラグを使用して操作を遅延させる**
    
    メソッドで\_一括バッチフラグを設定すると、テーブルの実装者は、そのうちの1つに処理する前に、複数の呼び出しを収集できます。 リモートサーバーに対して多くの呼び出しを行う代わりに、テーブルの実装者は、すべての操作を一度に実行することができます。 操作の結果は、必要になるまで評価されません。 
    
    たとえば、クライアントが[imapitable:: Restrict](imapitable-restrict.md)を呼び出して、\_一括バッチフラグが設定された制限を指定する場合、クライアントが[imapitable:: QueryRows](imapitable-queryrows.md)を呼び出してデータを取得するまで、制限を有効にする必要はありません。 これにより、テーブルの実装側は2つの呼び出しの作業を1つにまとめることができます。 表ユーザーのテーブルフラグを利用する\_ユーザーは、このような条件下でのエラー処理がより複雑になることに注意してください。 
    
    遅延操作でエラーを処理することは、mapi\_の DEFERRED_ERRORS フラグが設定されている場合にエラーを処理するのと似ています。詳細については、「 [mapi エラーの遅延](deferring-mapi-errors.md)」を参照してください。 
    
- **よく使用されるプロパティのキャッシュを保持する**
    
    テーブルを実装するサービスプロバイダーは、よく使用されるオブジェクトプロパティのコピーをキャッシュすることによって、ビューを作成するのにかかる時間を短縮できます。 これらのプロパティのコピーをメモリに保持すると、ビューを再構築するたびにオブジェクトからそれらのプロパティを取得する手間が省けます。
    
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

