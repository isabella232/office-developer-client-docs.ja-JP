---
title: プロパティの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd0f25f20c9e628a80d27f2b70e01dacc98229b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803709"
---
# <a name="property-types"></a>プロパティの種類

  
  
**適用されます**: Outlook 
  
MAPI には、単一値および複数値プロパティの両方がサポートされています。 単一値プロパティが、プロパティの基本型の値です。 複数値プロパティでは、基本データ型の複数の値があります。 
  
MAPI をサポートする単一値と複数値のプロパティの型は、次の表で説明します。 対応する複数値型を持つ単一値タイプごとに複数値型後ろにかっこで囲まれた単一値の型。
  
|**プロパティの種類**|**16 進値**|**説明**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |プロパティの型が不明であることを示します。 このプロパティの型は、インターフェイス メソッドを使用するため予約されています。  <br/> |
|PT_NULL  <br/> |0001  <br/> |プロパティの値がないことを示します。 このプロパティの種類は、インターフェイス メソッドで使用するため予約されており、VT_ を入力、OLE と同じです。  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |16 ビット (2 バイト) の符号付き整数。 このプロパティの種類は、PT_SHORT (PT_MV_SHORT) と OLE VT_I2 を入力と同じです。  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |符号付きまたは符号なし 32 ビット (4 バイト) の整数です。 このプロパティの種類は、PT_LONG (PT_MV_LONG) と、OLE は、VT_I4 を入力と同じです。  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32 ビット (8 ビット) 浮動小数点値です。 このプロパティの種類は、PT_R4 (PT_MV_R4) と OLE 型 VT_R4。  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64 ビット (8 ビット) 浮動小数点値です。 このプロパティの種類は、PT_R8 および VT_R8 と VT_DOUBLE は、OLE タイプと同じです。  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64 ビット (8 バイト) の整数値は、10 進数として解釈されます。 この種類のプロパティは、Microsoft Visual Basic の通貨の種類と互換性のある VT_CY を型、OLE と同じ。  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Double 型の値の日付と時刻として解釈されます。 日付は、整数部と小数部は時刻をです。 このプロパティの種類 VT_DATE OLE の種類と同じで、Microsoft Visual Basic の時刻の形式と互換性があります。  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE の値です。32 ビット (4 バイト) の符号なし整数。 この種類のプロパティは、OLE 型 VT_ERROR として同じです。  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16 ビット (2 バイト) のブール値 0 が 0 でない**場合は true**や**false**と等しい。 このプロパティの種類は、OLE タイプ VT_BOOL と同じです。  <br/> |
|PT_OBJECT  <br/> |000 D  <br/> |**IUnknown**インターフェイスを実装するオブジェクトへのポインター。 このプロパティの種類は、いくつかの種類の OLE VT_UNKNOWN などに似ています。  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |**LARGE_INTEGER**構造体を使用する符号付きまたは符号なしの 64 ビット (8 バイト) 整数。 このプロパティの種類は、PT_I8 と OLE VT_I8 を入力すると同じです。  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |8 ビット (2 バイト) 文字の null で終わる文字列。 この種類のプロパティは、OLE の種類の VT_LPSTR と同じです。  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |16 ビット (2 バイト) 文字の null で終わる文字列。 この型のプロパティには、UNICODE シンボルでコンパイルしないと、UNICODE のシンボルでコンパイルするときに PT_UNICODE と PT_STRING8 をリセットするプロパティの型があります。 このプロパティの種類は、PT_UNICODE プロパティの結果として得られる PT_STRING8 プロパティと VT_LPWSTR の OLE 型 VT_LPSTR と同じ  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |**FILETIME**構造体の形式でデータと時刻の値を 64 ビット (8 バイト) の整数です。 この種類のプロパティは、OLE の種類の VT_FILETIME と同じです。  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID**の構造体の値。 この種類のプロパティは、OLE の種類の VT_CLSID と同じです。  <br/> |
|PT_SVREID  <br/> |00 FB  <br/> |変数のサイズ、構造体の後に 16 ビット (2 バイト)**の数**です。  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |可変サイズの制限の 1 つまたは複数の構造を表すバイト配列。  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |可変サイズは、操作 (バイトではなく) の 16 ビット (2 バイト)**数**の後にするルールの処理の多くの構造体。  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary**構造体の値、長さのバイト配列。  <br/> |
   
> [!NOTE]
> 複数値を持つプロパティの型、または、PT_MV の 16 進数の値を指定するフラグ (0x00001000) プロパティの 16 進数の値を入力します。 など、16 進数の値 PT_MV_UNICODE は、0x101F、PT_MV_BINARY の 16 進値 0x1102。 
  

