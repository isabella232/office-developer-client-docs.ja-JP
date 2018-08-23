---
title: テーブルを使用したプロパティの操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804189"
---
# <a name="using-a-table-to-work-with-properties"></a>テーブルを使用したプロパティの操作

  
  
**適用対象**: Outlook 
  
多くのプロパティでは、オブジェクトがサポートするからとテーブルの列の両方が利用できます。 可能な限り、これらのプロパティをテーブルを取得します。
  
すべてのクライアントが必要なプロパティを含めるには、 [IMAPITable::SetColumns](imapitable-setcolumns.md)とすべてのテーブルの行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 
  
これら 2 つの呼び出しでは、通常、ユーザーに表示するには、十分な情報を取得するため、不要なオブジェクトを開くことに**OpenEntry**呼び出しを行う、必要な内部処理のための十分な頻繁にします。 
  
2 つだけ例外があります。
  
- プロパティが 255 バイトを超える場合。 * * IMAPITable * * インターフェイスは、代わりにそれを 255 バイトに切り捨て、全体のプロパティの値を返さない可能性があります。 このトレードオフをも考えてください。 ユーザーに、このデータを表示している場合は、255 バイトは、コメントなどのテキスト フィールドには十分で可能性があります。 
    
- 場合は、テーブル内の 1 つの行から特定のプロパティが必要です。 ここで使用することはありませんプロパティを持つテーブルを作成する必要はありません。 時間のほとんどすべての行の同じプロパティを必要があります。
    

