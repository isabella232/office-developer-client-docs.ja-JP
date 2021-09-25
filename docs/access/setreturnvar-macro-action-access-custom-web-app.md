---
title: SetReturnVar マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: SetReturnVar/戻り変数の設定アクションは、戻り変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: 0560ec9b1d4adbe215e5c187bcc1135c605b3ee9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614746"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar マクロ アクション (Access カスタム Web アプリ)

" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**SetReturnVar**/戻り変数の設定" アクションは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

"**SetReturnVar**/戻り変数の設定" アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
| _名前_ <br/> |はい  <br/> |変数の名前を指定する文字列。  <br/> |
| _Expression_ <br/> |はい  <br/> |An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  <br/> |
   
## <a name="remarks"></a>注釈

"**SetReturnVar**/戻り変数の設定" アクションを使用して、変数の **ReturnVar** を作成できます。この変数を、"**RunDataMacro**/データマクロの実行" アクションを使用してデータ マクロを呼び出すマクロで使用できます。 
  
**SetReturnVar** アクションによって **ReturnVar** が作成されると、呼び出し元のマクロは式で使用できます。 たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。
  
`=[ReturnVars]![UpdateSuccess]`

" **SetReturnVar** /戻り変数の設定" アクションは、名前付きのデータ マクロでのみ使用できます。これを、データ マクロ イベントに接続されたデータ マクロで使用できません。 
  

