---
title: FONT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: 名前で指定されたフォントの一意識別子の整数値を返します。
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422174"
---
# <a name="font-function"></a>FONT 関数

名前で指定されたフォントの一意識別子の整数値を返します。
  
> [!NOTE]
> ほとんどの場合、フォント識別子はシステム固有です。 フォントはファイル内で使用された後も確立されたままですが、**フォント**関数を使用すると、Visio のシステムおよびバージョン間で特定のフォントに一貫したアクセスが可能になります。 フォント識別子を直接参照するのではなく、**FONT** 関数を使用してフォントを割り当てることをお勧めします。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **フォント**( _"font_name_string"_)
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |必須  <br/> |**string** <br/> |フォントの名前。  <br/> |
   
## <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

*font_name_string*に指定された文字列が既知のフォントと一致しない場合、この関数は #VALUE を返します。 エラーを返します。 
  
## <a name="example"></a>例

 `FONT("Calibri")`
  
"Calibri" フォントの一意の ID を表す整数値 (4) を返します。
  

