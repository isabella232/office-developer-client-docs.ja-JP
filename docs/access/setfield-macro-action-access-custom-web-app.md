---
title: setfield マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: SetField/フィールドの設定アクションでは、フィールドに値を割り当てることができます。
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432927"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>setfield マクロアクション (Access カスタム web アプリ)

The **SetField** action can be used to assign a value to a field. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**SetField**/フィールドの設定" アクションは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

"**SetField**/フィールドの設定" アクションの引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
|**名前** <br/> |フィールドを識別する文字列。  <br/> |
|**値** <br/> |フィールドに割り当てる値を指定する式。  <br/> |
   
## <a name="remarks"></a>注釈

" **SetField** /フィールドの設定" アクションは、 **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** データ ブロック外または **[EditRecord](editrecord-data-block-access-custom-web-app.md)** データ ブロック外では使用できません。 
  

