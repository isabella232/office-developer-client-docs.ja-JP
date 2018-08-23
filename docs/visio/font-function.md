---
title: FONT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: 名前で指定されたフォントの一意識別子の整数値を返します。
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805427"
---
# <a name="font-function"></a>FONT 関数

名前で指定されたフォントの一意識別子の整数値を返します。
  
> [!NOTE]
> ほとんどの場合は、フォントの識別子は、システム固有です。 フォントは、ファイルで使用して 1 回確立されたままが**フォント**関数は、システムおよび Visio のバージョン間で特定のフォントを一貫したアクセスを提供します。 フォントの識別子への参照を直接ではなくフォントを割り当てるには、**フォント**機能を使用することをお勧めします。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **フォント**( _"font_name_string"_)
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |必須  <br/> |**string** <br/> |フォント名を指定します。  <br/> |
   
## <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

*Font_name_string*の指定された文字列で、フォントが一致しない場合、この関数は、#VALUE を返します。 エラーを返します。 
  
## <a name="example"></a>例

 `FONT("Calibri")`
  
「Calibri」フォントには、一意 ID を表す整数値 (4) を返します。
  

