---
title: 列と制限の設定後のテーブルの並べ替え
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409882"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>列と制限の設定後のテーブルの並べ替え

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
並べ替えたテーブルのビューを制限する必要がある場合は、常に次の **IMAPITable** 呼び出しを次の順序で行います。 
  
1. [列セットを定義する IMAPITable::SetColumns。](imapitable-setcolumns.md) 
    
2. [IMAPITable::制限を適用](imapitable-restrict.md) します。 
    
3. [IMAPITable::SortTable を使用して](imapitable-sorttable.md) 並べ替えを実行します。 
    
並べ替えたテーブルが分類されている場合は、SortTable 呼び出しの後、必要に応じて [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)を **呼び出** します。 ほとんどのサービス プロバイダーは、最高のパフォーマンスを得る最後のタスクとしてテーブルを並べ替えるので、この呼び出しの順序付けは重要です。 たとえば、メッセージ ストア プロバイダーが制限を適用する前にフォルダーコンテンツ テーブルを分類する必要がある場合、この分類は制限の処理中に削除されます。 2 番目の分類が必要になります。 
  

