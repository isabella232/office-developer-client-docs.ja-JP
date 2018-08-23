---
title: OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: ポップアップ ・ ウィンドウで指定されたビューを開きます。
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798706"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup マクロのアクション (カスタム web アプリケーションのアクセス)

ポップアップ ・ ウィンドウで指定されたビューを開きます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **OpenPopup**(*ビュー*、 *、=*、*順*) 
  
**OpenPopup**アクションには、次の引数が含まれています。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *View*  <br/> |開くビューの名前を指定します。  <br/> |
| *場所 =*  <br/> |有効な SQL WHERE 句 (単語なしで) ビュー内のレコードを制限しています。  <br/> |
| *Order By/並び替え*  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

**OpenPopup**アクションを処理すると、現在のマクロが終了します。 
  
**OpenPopup**アクションが呼び出されたときに、並べ替え、またはユーザーによって適用されたフィルターがクリアされます。 
  
*並べ替え*引数は、フィールドまたはレコードをソートするフィールドの名前です。 複数のフィールド名を指定する場合はコンマ (,) で区切ります。 
  
*並べ替え*引数を設定すると、既定では昇順でレコードが並べ替えられます。 
  

