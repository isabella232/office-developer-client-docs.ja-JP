---
title: SetField マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: SetField/フィールドの設定アクションでは、フィールドに値を割り当てることができます。
ms.openlocfilehash: 95928aa85e09ef1f5d2b58fa2a02a33c32ebec49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605737"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>SetField マクロ アクション (Access カスタム Web アプリ)

The **SetField** action can be used to assign a value to a field. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**SetField**/フィールドの設定" アクションは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

"**SetField**/フィールドの設定" アクションの引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
|**名前** <br/> |フィールドを識別する文字列。  <br/> |
|**値** <br/> |フィールドに割り当てる値を指定する式。  <br/> |
   
## <a name="remarks"></a>注釈

" **SetField** /フィールドの設定" アクションは、 **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** データ ブロック外または **[EditRecord](editrecord-data-block-access-custom-web-app.md)** データ ブロック外では使用できません。 
  

