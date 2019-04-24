---
title: プロパティの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328491"
---
# <a name="property-types"></a>プロパティの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI では、単一値プロパティと複数値プロパティの両方がサポートされています。 単一値のプロパティを使用すると、プロパティの基本型の値が1つあります。 複数値プロパティを使用すると、基本型に複数の値が存在します。 
  
次の表では、MAPI がサポートする単一値と複数値のプロパティの種類について説明します。 対応する複数値の型を持つ単一の値の型に対して、複数値の型は、単一値の型の後にかっこで囲んで表示されます。
  
|**プロパティの種類**|**16進値**|**説明**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |プロパティの種類が不明であることを示します。 このプロパティの種類は、インターフェイスメソッドで使用するために予約されています。  <br/> |
|PT_NULL  <br/> |0001  <br/> |プロパティ値がないことを示します。 このプロパティの種類は、インターフェイスメソッドで使用するために予約されており、OLE 型 VT_NULL と同じです。  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |符号付き16ビット (2 バイト) 整数。 このプロパティの種類は、PT_SHORT (PT_MV_SHORT) および OLE type VT_I2 と同じです。  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |符号付きまたは符号なしの32ビット (4 バイト) 整数。 このプロパティの種類は、PT_LONG (PT_MV_LONG) および OLE type VT_I4 と同じです。  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32ビット (8 バイト) 浮動小数点値。 このプロパティの種類は、PT_R4 (PT_MV_R4) および OLE type VT_R4 と同じです。  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64ビット (8 バイト) 浮動小数点値。 このプロパティの種類は、PT_R8 と OLE の種類 VT_R8 および VT_DOUBLE と同じです。  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64ビット (8 バイト) 整数は、10進数として解釈されます。 このプロパティの種類は、Microsoft Visual Basic の通貨の種類と互換性があり、OLE type VT_CY と同じです。  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |日付と時刻として解釈される倍精度浮動小数点型 (Double) の値です。 整数部分は日付で、小数部分は時刻です。 このプロパティの型は、OLE type VT_DATE と同じで、Microsoft Visual Basic の時刻表現と互換性があります。  <br/> |
|PT_ERROR  <br/> |000a  <br/> |SCODE 値。32ビット (4 バイト) の符号なし整数。 このプロパティの型は、OLE type VT_ERROR と同じです。  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |0が**false**で0以外の値が**true**の場合、16ビット (2 バイト) のブール値。 このプロパティの型は、OLE type VT_BOOL と同じです。  <br/> |
|PT_OBJECT  <br/> |000d  <br/> |**IUnknown**インターフェイスを実装するオブジェクトへのポインター。 このプロパティの種類は、VT_UNKNOWN などのいくつかの OLE の種類に似ています。  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |**LARGE_INTEGER**構造体を使用する、符号付きまたは符号なしの64ビット (8 バイト) 整数。 このプロパティの種類は、PT_I8 および OLE type VT_I8 と同じです。  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001e  <br/> |Null で終了した8ビット (2 バイト) 文字の文字列。 このプロパティの型は、OLE type VT_LPSTR と同じです。  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001f  <br/> |Null で終端された16ビット (2 バイト) 文字列。 この型のプロパティは、unicode 記号を使用してコンパイルする場合はプロパティの種類を PT_UNICODE に、unicode 記号を使用してコンパイルしない場合は PT_STRING8 に設定します。 このプロパティの型は、結果として得られる PT_STRING8 properties および VT_LPWSTR の OLE type VT_LPSTR と同じです。  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64ビット (8 バイト) 整数データと時刻値を、 **FILETIME**構造体の形式で指定します。 このプロパティの型は、OLE type VT_FILETIME と同じです。  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID**構造の値。 このプロパティの型は、OLE type VT_CLSID と同じです。  <br/> |
|PT_SVREID  <br/> |00fb  <br/> |可変サイズ、16ビット (2 バイト)、その後**** に構造が続きます。  <br/> |
|PT_SRESTRICT  <br/> |00fd  <br/> |可変サイズ。1つまたは複数の制限構造を表すバイト配列。  <br/> |
|PT_ACTIONS  <br/> |00fe  <br/> |可変サイズ、16ビット (2 バイト) のアクション数**** (バイトではない) の後に、多くのルールアクション構造が続きます。  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**sbinary**構造体の値。カウントされたバイト配列。  <br/> |
   
> [!NOTE]
> 複数値を持つプロパティの種類の16進値を確認するには、または、PT_MV フラグ (0x00001000) をプロパティの種類の16進値に設定します。 たとえば、PT_MV_UNICODE の16進値は0x101F で、PT_MV_BINARY の16進値は0x1102 です。 
  

