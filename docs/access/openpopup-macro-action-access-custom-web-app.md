---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: 指定したビューをポップアップウィンドウで開きます。
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427389"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)

指定したビューをポップアップウィンドウで開きます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **openpopup**(*ビュー*、 *Where =*、 *Order By*) 
  
**openpopup**アクションには、次の引数が含まれています。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *View*  <br/> |開くビューの名前を指定します。  <br/> |
| *Where =*  <br/> |ビュー内のレコードを制限する有効な SQL where 句 (単語 where を除く)。  <br/> |
| *Order By/並び替え*  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

**openpopup**アクションが処理されると、現在のマクロは終了します。 
  
**openpopup**アクションが呼び出されると、ユーザーによって適用されたすべての並べ替えまたはフィルター処理がクリアされます。 
  
The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). 
  
When you set the  *OrderBy*  argument, the records are sorted by default in ascending order. 
  

