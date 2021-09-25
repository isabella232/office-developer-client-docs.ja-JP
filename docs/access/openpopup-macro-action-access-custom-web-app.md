---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: ポップアップ ウィンドウで指定したビューを開きます。
ms.openlocfilehash: f381389dad13e2a31fa73009118804ed5588c048
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576815"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)

ポップアップ ウィンドウで指定したビューを開きます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
**OpenPopup アクションには**、次の引数が含まれます。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *View*  <br/> |開くビューの名前を指定します。  <br/> |
| *Where=*  <br/> |ビュー内SQLを制限する WHERE 句 (WHERE という単語を含む) を指定します。  <br/> |
| *Order By/並び替え*  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

OpenPopup アクションが処理 **された後、現在の** マクロは終了します。 
  
ユーザーが適用した並べ替えまたはフィルター処理は **、OpenPopup** アクションが呼び出されるとクリアされます。 
  
The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). 
  
When you set the  *OrderBy*  argument, the records are sorted by default in ascending order. 
  

