---
title: RequeryRecords マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: RequeryRecords アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798724"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords マクロのアクション (カスタム web アプリケーションのアクセス)

**RequeryRecords** アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**RequeryRecords** アクションの引数は次のとおりです。 
  
|**パラメーター**|**必須**|**説明**|
|:-----|:-----|:-----|
|**場所 =** <br/> |いいえ  <br/> |ビュー内のレコードを制限する SQL WHERE 句。既定では、この引数は空白です。  <br/> |
|**OrderBy** <br/> |いいえ  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

**RequeryRecords** アクションが呼び出されたとき、すべての並べ替え、またはユーザーにより適用されたフィルター処理はオフにされます。 
  
*並べ替え*引数は、フィールドまたはレコードをソートするフィールドの名前です。 複数のフィールド名を指定する場合はコンマ (,) で区切ります。 
  
*並べ替え*引数を設定すると、既定では昇順でレコードが並べ替えられます。 
  
降順でレコードを並べ替えるには、 *OrderBy*の引数の式の末尾に DESC を入力します。 などの顧客レコードを取引先担当者の名前で降順に並べ替えるには、 *OrderBy*引数を"得意先コード DESC"を設定します。 
  
降順で、姓と名の昇順で名前を並べ替えるには、」「姓 desc, FirstName ASC" *OrderBy*引数を設定します。 
  

