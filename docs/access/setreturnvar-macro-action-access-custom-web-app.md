---
title: SetReturnVar マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: SetReturnVar/戻り変数の設定アクションは、戻り変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798758"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar マクロのアクション (カスタム web アプリケーションのアクセス)

" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> [!メモ] " **SetReturnVar/戻り変数の設定** " アクションは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

" **SetReturnVar/戻り変数の設定** " アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
| _名前_ <br/> |はい  <br/> |変数の名前を指定する文字列。  <br/> |
| _Expression_ <br/> |はい  <br/> |この一時変数の値を設定に使用する式を指定します。 式の前に等号 (=) を付けないでください。 この引数を設定するのには、**式ビルダー**を使用するのには [**ビルド**] ボタンをクリックすることができます。  <br/> |
   
## <a name="remarks"></a>注釈

" **SetReturnVar/戻り変数の設定** " アクションを使用して、 **ReturnVar** を作成します。この変数は、" **RunDataMacro/データマクロの実行** " アクションを使用してデータ マクロを呼び出すマクロが使用できます。 
  
**SetReturnVar**アクションによって、 **ReturnVar**が作成されると、呼び出し元のマクロで使用できます、式。 たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。
  
`=[ReturnVars]![UpdateSuccess]`

" **SetReturnVar** /戻り変数の設定" アクションは、名前付きのデータ マクロでのみ使用できます。これを、データ マクロ イベントに接続されたデータ マクロで使用できません。 
  

