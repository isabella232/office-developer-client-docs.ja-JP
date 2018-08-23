---
title: テーブルの行からデータを所得する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803771"
---
# <a name="retrieving-data-from-table-rows"></a>テーブルの行からデータを所得する

  
  
**適用対象**: Outlook 
  
テーブルから行を取得する必要があります。
  
- すべての列のプロパティ値を取得します。
    
- 現在の位置を変更します。
    
エントリ id は、ほとんどのテーブルで必要な列のいずれかの- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、行を表すオブジェクトを開くことを使用することができます。 このエントリ id は、通常、いずれかのテーブルの有効期間を超えて保持されませんが、短期的なエントリ id です。 ただし、テーブルのみを実装するサービス プロバイダーは、エントリの識別子の 1 つの型をサポートしている場合長期的な識別子である、ことができます。
  
クライアントとサービス ・ プロバイダーは、以下の行を取得する呼び出しのいずれかで作成できます。
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |前方または後方のいずれかの方向の現在の行で始まる行の指定した数を取得します。  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |すべてのテーブルの行を取得します。  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |そのインデックス列の値に基づいてテーブルの行を取得します。 **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、通常、テーブルのインデックスの列です。  <br/> |
   
オプションのプロパティは、テーブル内の列の 1 つとして含まれているが、他のユーザーは実行できないときに、列の有効な値がいくつかの行のがあります。 列の有効な値が存在するかどうかは、行の情報を提供するオブジェクトがプロパティを設定するかどうかによって異なります。 オブジェクトの実装によって**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) として、テーブル、または任意の値で存在しないプロパティを表すことができます。 テーブルのユーザーが存在しないし、無意味な値を持つプロパティとプロパティは存在し、有効な値であることの間で区別するために注意が必要である必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

