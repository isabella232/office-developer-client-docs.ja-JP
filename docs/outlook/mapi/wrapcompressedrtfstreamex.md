---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391732"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**適用対象**: Outlook 2013 | Outlook 2016 
  
圧縮解除で圧縮されたリッチ テキスト形式式 (RTF)、電子メール メッセージの本文圧縮解除ストリームの形式を指定、必要に応じてネイティブ形式、圧縮解除されたストリームに変換し、いずれかの圧縮解除されたストリームを返しますまたは、。ネイティブ ストリームを変換します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>パラメーター

_lpCompressedRTFStream_
  
> [in]これは、メッセージの[既定のプロパティの PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)で開かれているストリームへのポインターです。 
    
_pWCSInfo_
  
> [in]ポインターは、 
    
   関数のオプションを含む[について](rtf_wcsinfo.md)構造体です。 
    
_lppUncompressedRTFStream_
  
> [out]これは、圧縮解除の rtf 形式のストリームが返される位置の場所へのポインターです。 
    
_pRetInfo_
  
> [out]これは、返された圧縮解除ストリームの形式に関する情報が含まれている[この](rtf_wcsretinfo.md)構造体へのポインターです。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数の呼び出しが成功します。
    
MAPI_E_INVALID_PARAMETER 
  
- **MAPI_NATIVE_BODY**フラグは、 **ulFlags** 、**について**構造体のフィールドで示される*pWCSInfo*の**MAPI_MODIFY**フラグを使用している場合、この関数が返されます。 
    
## <a name="remarks"></a>備考

**WrapCompressedRTFStreamEx**は、ストリームを圧縮解除、圧縮された rtf 形式でカプセル化された電子メール メッセージの本文にアクセスできるように、圧縮解除されたストリームの形式では、および必要に応じてネイティブ形式の本文のストリームを返します。 ネイティブ形式の本文のストリームは、RTF、プレーン テキスト、または HTML で指定できます。 
  
Microsoft Office Outlook オブジェクト モデルでは、 **MailItem**オブジェクトおよび本文テキストの書式を示す[MailItem.BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)の**本文**のプロパティを提供します。 仕様では、Outlook で信頼されていないソリューションは、セキュリティに関するダイアログ ボックスで Outlook セキュリティ ガードの生成を呼び出します。 エクスポートされた MAPI 関数**WrapCompressedRTFStreamEx**を使用すると、MAPI を使用して、Outlook オブジェクト モデルではなく、これらのセキュリティ] ダイアログ ボックスを回避するソリューションができます。 
  
**MAPI\_NATIVE_BODY**とフラグを組み合わせることはできません、 **MAPI\_変更**の**ulFlags**フィールドのフラグ、 **RTF\_WCSINFO** *pWCSInfo*が指す構造体のみを使用するネイティブ読み取り専用モードで本文のストリーム。 読み取り/書き込みモードでのネイティブ形式の本文のストリームにアクセスするには、 **WrapCompressedRTFStream**関数を使用する必要があります。 
  
## <a name="see-also"></a>関連項目

- [圧縮 RTF 内のメッセージ本体を取り出し、ネイティブ形式に変換する](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

