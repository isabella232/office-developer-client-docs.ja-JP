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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344486"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>列と制限の設定後のテーブルの並べ替え

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
並べ替えられたテーブルの表示を制限する必要がある場合は、常に次の順序で**IMAPITable**呼び出しを行います。 
  
1. [IMAPITable:: SetColumns](imapitable-setcolumns.md)列セットを定義します。 
    
2. [IMAPITable::](imapitable-restrict.md)制限を課すことができます。 
    
3. [IMAPITable::](imapitable-sorttable.md)並べ替えを実行するための sorttable。 
    
並べ替えられたテーブルが分類されている場合は、必要に応じて**sorttable**の呼び出しの後に、 [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md)を呼び出します。 ほとんどのサービスプロバイダーは、最高のパフォーマンスを実現するために最後のタスクとしてテーブルを並べ替えるので、この呼び出しの順序は重要です。 たとえば、メッセージストアプロバイダーが、制限を設定する前にフォルダーの内容テーブルを分類する必要がある場合、この分類は制限の処理中に削除されます。 2番目の分類が必要になります。 
  

