---
title: Try_Convert関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: 指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 0e2aa0d877090812494c2aa53a3325ad2217eaa5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564681"
---
# <a name="try_convert-function-access-custom-web-app"></a>Try_Convert関数 (Access カスタム Web アプリ)

指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Try_Convert** (*DataType*, *Expression*) 
  
**Try_Convert** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DataType*  <br/> |式 を変換するデータ  *型*  です。  <br/> |
| *Expression*  <br/> |変換する値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

 **Try_Convert** は渡された値を取得し、指定された  *DataType*  への変換を試みます。変換が成功した場合、 **Try_Convert** は  *DataType*  で指定された型で値を返します。エラーが発生した場合は null が返されます。ただし、明示的に許可されていない変換を要求すると、 **Try_Convert** はエラーになって失敗します。 
  

