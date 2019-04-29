---
title: テーブルを使用したプロパティの操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439913"
---
# <a name="using-a-table-to-work-with-properties"></a>テーブルを使用したプロパティの操作

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのプロパティは、それらをサポートするオブジェクトとテーブルの列の両方で使用できます。 可能な場合は、テーブルを使用してこれらのプロパティを取得します。
  
[SetColumns](imapitable-setcolumns.md) :: QueryRows を呼び出して、クライアントが必要とするすべてのプロパティを含み、 [imapitable::](imapitable-queryrows.md)を使用して、テーブルのすべての行を取得します。 
  
通常、ユーザーに表示するのに十分な情報を取得し、必要な内部処理に十分な場合は、次の2つの呼び出しでは、オブジェクトを不必要に開く**openentry**を呼び出すことができます。 
  
次の2つの例外があります。
  
- プロパティが255バイトを超えている場合。 * * IMAPITable * * インターフェイスはプロパティ値全体を返さないことがあり、その代わりに255バイトで切り捨てます。 ただし、このトレードオフについて考えてみましょう。 このデータをユーザーに表示している場合は、コメントなどのテキストフィールドに対して255バイトで十分な場合があります。 
    
- テーブル内の単一の行の特定のプロパティが必要な場合。 この場合は、決して使用しないプロパティを持つテーブルを作成する必要はありません。 ほとんどの場合、すべての行に同じプロパティが必要になります。
    

