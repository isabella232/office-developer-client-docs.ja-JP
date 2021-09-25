---
title: FONT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: 名前で指定されたフォントの一意識別子の整数値を返します。
ms.openlocfilehash: 9211d56299cbf3085de4060921b19b6a0ed414e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574231"
---
# <a name="font-function"></a>FONT 関数

名前で指定されたフォントの一意識別子の整数値を返します。
  
> [!NOTE]
> ほとんどの場合、フォント識別子はシステム固有です。 フォントはファイルで一度使われると確立されたままですが **、FONT** 関数はシステムやバージョンのフォント間で特定のフォントに一貫したアクセスVisio。 フォント識別子を直接参照するのではなく、**FONT** 関数を使用してフォントを割り当てることをお勧めします。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **FONT**( _"font_name_string"_)
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |必須かどうか  <br/> |**string** <br/> |フォントの名前。  <br/> |
   
## <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

指定した文字列が既知の  *フォントfont_name_string*  一致しない場合、この関数は既知のフォントを#VALUE! エラーを返します。 
  
## <a name="example"></a>例

 `FONT("Calibri")`
  
"Calibri" フォントの一意の ID を表す整数値 (4) を返します。
  

