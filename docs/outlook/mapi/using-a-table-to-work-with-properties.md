---
title: テーブルを使用したプロパティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: abef70e2d5e9fc2eef1ae07f33552c84ecbe9e23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609209"
---
# <a name="using-a-table-to-work-with-properties"></a>テーブルを使用したプロパティの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのプロパティは、それらをサポートするオブジェクトとテーブルの列の両方から使用できます。 可能な限り、これらのプロパティをテーブルから取得します。
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出して、クライアントで必要なすべてのプロパティを含め[、IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出して、テーブルのすべての行を取得します。 
  
これらの 2 つの呼び出しは、通常、ユーザーに表示するのに十分な情報を取得するのに十分であり、必要な内部処理を行う場合は多くの場合 **、OpenEntry** を呼び出してオブジェクトを不要に開くのに十分です。 
  
次の 2 つの例外があります。
  
- プロパティが 255 バイトを超える場合。 ** IMAPITable ** インターフェイスは、プロパティ値全体を返すのではなく、255 バイトで切り捨てることはできません。 しかし、このトレードオフについて考えてみろ。 このデータをユーザーに表示する場合は、コメントなどのテキスト フィールドで 255 バイトで十分です。 
    
- テーブル内の 1 行から特定のプロパティが必要な場合。 この場合、使用しないプロパティを持つテーブルを作成する必要があります。 ほとんどの場合、すべての行に同じプロパティが必要になります。
    

