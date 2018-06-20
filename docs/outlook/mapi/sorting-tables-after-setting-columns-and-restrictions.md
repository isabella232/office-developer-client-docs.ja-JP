---
title: 列と制約を設定した後のテーブルの並べ替え
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803988"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>列と制約を設定した後のテーブルの並べ替え

  
  
**適用されます**: Outlook 
  
並べ替えられたテーブルのビューを制限するには、常に確認する必要があります次**IMAPITable**は次の順序で呼び出されます。 
  
1. 列を定義する[IMAPITable::SetColumns](imapitable-setcolumns.md)を設定します。 
    
2. [IMAPITable::Restrict](imapitable-restrict.md)の制限を適用します。 
    
3. [IMAPITable::SortTable](imapitable-sorttable.md)の並べ替えを実行します。 
    
ソート後のテーブルを分類すると場合、呼び出しを行う[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)、必要に応じて、 **SortTable**の呼び出しの後です。 ほとんどのサービス プロバイダーは、最高のパフォーマンスを達成するために最後のタスクとしてテーブルを並べ替えるために、この呼び出しの順序が重要です。 などの制限が適用される前に、メッセージ ストア プロバイダーはフォルダーの内容のテーブルを分類する必要がある場合は、この分類は、制限の処理中に削除されます。 2 つ目の分類は、必要があります。 
  

