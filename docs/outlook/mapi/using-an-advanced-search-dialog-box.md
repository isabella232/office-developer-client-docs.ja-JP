---
title: '[高度な検索] ダイアログボックスを使用する'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329667"
---
# <a name="using-an-advanced-search-dialog-box"></a>[高度な検索] ダイアログボックスを使用する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳のコンテナーには、クライアントが**PR_DISPLAY_NAME**以外のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を検索できる高度な検索機能をサポートしているものがあります。 高度な検索をサポートするアドレス帳コンテナーには、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) という名前のコンテナーオブジェクトプロパティがあります。 この container オブジェクトは、[検索] ダイアログボックスについて説明する表示テーブルへのアクセスを提供します。このダイアログボックスは、高度な検索条件を入力および編集するために使用されます。
  
 **アドレス帳コンテナーに対して高度な検索を実行するには**
  
1. コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、プロパティタグと IID_IMAPIContainer のインターフェイス識別子に**PR_SEARCH**を指定します。 
    
2. **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) をプロパティタグと IID_IMAPITable のインターフェイス識別子に指定して、search オブジェクトの**imapiprop:: openproperty**メソッドを呼び出します。 
    
3. 検索オブジェクトの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、高度な検索で使用されるプロパティの値を設定します。 
    
4. 検索オブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、高度な検索条件を保存します。 
    
この一連の呼び出しでは、クライアントが search オブジェクトの**getsearchcriteria**メソッドを呼び出すときに、制限が有効になります。 
  

