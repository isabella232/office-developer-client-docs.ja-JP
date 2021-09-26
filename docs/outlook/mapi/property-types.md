---
title: プロパティの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d211426240d5bee73c1afb59d8905fefa727e6fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624392"
---
# <a name="property-types"></a>プロパティの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI では、単一値プロパティと複数値プロパティの両方がサポートされています。 単一値のプロパティでは、プロパティの基本型の値が 1 つ指定されます。 複数値プロパティを使用すると、基本型の値が複数ある。 
  
MAPI でサポートされる単一値および複数値のプロパティの種類を次の表に示します。 対応する複数値型を持つ単一値型ごとに、単一値型の後に複数値型がかっこで囲んで表示されます。
  
|**プロパティの種類**|**16 進数の値**|**説明**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |プロパティの種類が不明です。 このプロパティの種類は、インターフェイス メソッドで使用するために予約されています。  <br/> |
|PT_NULL  <br/> |0001  <br/> |プロパティ値なしを示します。 このプロパティの種類は、インターフェイス メソッドで使用するために予約され、OLE 型と同VT_NULL。  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |符号付き 16 ビット (2 バイト) の整数。 このプロパティの種類は、(PT_SHORT) PT_MV_SHORT OLE 型と同VT_I2。  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |符号付きまたは符号なし 32 ビット (4 バイト) の整数。 このプロパティの種類は、(PT_LONG) PT_MV_LONG OLE 型と同VT_I4。  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32 ビット (8 バイト) 浮動小数点値。 このプロパティの種類は、(PT_R4) PT_MV_R4 OLE 型と同VT_R4。  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64 ビット (8 バイト) 浮動小数点値。 このプロパティの種類は、OLE の種類PT_R8と同じVT_R8とVT_DOUBLE。  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY )  <br/> |0006  <br/> |64 ビット (8 バイト) の整数を 10 進数と解釈します。 このプロパティの種類は、Microsoft の通貨Visual Basicと互換性があり、OLE の種類と同VT_CY。  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |日付と時刻として解釈される倍数の値。 整数部分は日付で、分数部分は時刻です。 このプロパティの種類は、OLE の種類と同VT_DATE、Microsoft の時刻表記Visual Basic互換性があります。  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE 値。32 ビット (4 バイト) の符号なし整数。 このプロパティの種類は、OLE の種類と同VT_ERROR。  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16 ビット (2 バイト) のブール値で、ゼロが **false、** ゼロ以外が **true です**。 このプロパティの種類は、OLE の種類と同VT_BOOL。  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |**IUnknown** インターフェイスを実装するオブジェクトへのポインター。 このプロパティの種類は、次のような複数の OLE 型に似VT_UNKNOWN。  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |符号付きまたは符号なしの 64 ビット (8 バイト) **の** 整数で、この構造体をLARGE_INTEGERします。 このプロパティの種類は、次のプロパティPT_I8 OLE 型と同VT_I8。  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Null で終端された 8 ビット (2 バイト) の文字列。 このプロパティの種類は、OLE の種類と同VT_LPSTR。  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Null で終端された 16 ビット (2 バイト) の文字列。 この型のプロパティは、UNICODE シンボルを使用してPT_UNICODE、UNICODE シンボルを使用してコンパイルしない場合PT_STRING8プロパティの種類がリセットされます。 このプロパティの種類は、結果のプロパティの OLE VT_LPSTRとPT_STRING8プロパティVT_LPWSTR同PT_UNICODEです。  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |FILETIME 構造体の形式の 64 ビット (8 バイト) の整数データと **時間値** 。 このプロパティの種類は、OLE の種類と同VT_FILETIME。  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID** 構造体の値。 このプロパティの種類は、OLE の種類と同VT_CLSID。  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |可変サイズ、16 ビット (2 バイト) **の COUNT** の後に構造体が続きます。  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |可変サイズ、1 つ以上の Restriction 構造体を表すバイト配列。  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |可変サイズ、16 ビット (2 バイト) のアクションの **COUNT** (バイトではなく) の後に多数の Rule Action 構造体が続きます。  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary 構造体** の値、カウントされたバイト配列。  <br/> |
   
> [!NOTE]
> 複数値を持つプロパティの種類の 16 進数の値を確認するには、プロパティの種類の hex 値PT_MVフラグ (0x00001000) を指定します。 たとえば、値の 16 進値PT_MV_UNICODE、0x101Fの Hex 値がPT_MV_BINARYされます0x1102。 
  

