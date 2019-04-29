---
title: RequeryRecords マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: RequeryRecords アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439248"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords マクロアクション (Access カスタム web アプリ)

**RequeryRecords** アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**RequeryRecords** アクションの引数は次のとおりです。 
  
|**パラメーター**|**必須**|**説明**|
|:-----|:-----|:-----|
|**Where =** <br/> |いいえ  <br/> |ビュー内のレコードを制限する SQL WHERE 句。既定では、この引数は空白です。  <br/> |
|**OrderBy** <br/> |いいえ  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

**RequeryRecords** アクションが呼び出されたとき、すべての並べ替え、またはユーザーにより適用されたフィルター処理はオフにされます。 
  
The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). 
  
When you set the  *OrderBy*  argument, the records are sorted by default in ascending order. 
  
To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression. For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC". 
  
To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC". 
  

