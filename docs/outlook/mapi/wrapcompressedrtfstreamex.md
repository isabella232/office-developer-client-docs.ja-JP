---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e312388a86e4b93806a7d2884884c90f570fa03e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590871"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**適用対象**: Outlook 2013 | Outlook 2016 
  
圧縮リッチ テキスト形式 (RTF) の電子メール メッセージの本文を圧縮解除し、圧縮解除されたストリームの形式を示し、必要に応じて圧縮解除されたストリームをネイティブ形式に変換し、圧縮解除されたストリームまたは変換されたネイティブ ストリームを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
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
  
> [in]これは、メッセージの [PidTagRtfCompressed Canonical プロパティ](pidtagrtfcompressed-canonical-property.md) で開くストリームへのポインターです。 
    
_pWCSInfo_
  
> [in]これは、a を指すポインターです。 
    
   [RTF_WCSINFO](rtf_wcsinfo.md) オプションを含む構造を指定します。 
    
_lppUncompressedRTFStream_
  
> [out]これは、圧縮解除された RTF のストリームが返される場所へのポインターです。 
    
_pRetInfo_
  
> [out]これは、返される圧縮解除 [されたRTF_WCSRETINFO](rtf_wcsretinfo.md) 形式に関する情報を含むオブジェクト構造へのポインターです。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
MAPI_E_INVALID_PARAMETER 
  
- これは *、pWCSInfo* が指す **RTF_WCSINFO** 構造体の **ulFlags** フィールドの **MAPI_MODIFY** フラグと MAPI_NATIVE_BODY フラグを組み合 **わせた** 場合に返されます。 
    
## <a name="remarks"></a>注釈

**WrapCompressedRTFStreamEx** を使用すると、ストリームを解凍して圧縮された RTF にカプセル化された電子メール メッセージの本文にアクセスし、圧縮解除されたストリームとその形式、およびオプションでネイティブ本文ストリームを返します。 ネイティブ本文ストリームは、RTF、プレーン テキスト、または HTML で指定できます。 
  
オブジェクト Microsoft Office Outlookは **、MailItem** オブジェクトの Body プロパティと、本文テキストの形式を示す [MailItem.BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)を提供します。 設計上、セキュリティ ガードによって信頼されていないソリューションは、Outlook Security Guard によって生成されたセキュリティ ダイアログ ボックスOutlook呼び出します。 エクスポートされた MAPI 関数 **WrapCompressedRTFStreamEx** を使用すると、ソリューションは Outlook オブジェクト モデルではなく MAPI を使用し、これらのセキュリティ ダイアログ ボックスを回避できます。 
  
MAPI **\_ NATIVE_BODY** フラグを *pWCSInfo* が指す **RTF \_ WCSINFO** 構造体の **ulFlags** フィールドの **MAPI \_ MODIFY** フラグと組み合わせはできないので、読み取り専用モードでのみネイティブ本文ストリームにアクセスできます。 読み取り/書き込みモードでネイティブ本文ストリームにアクセスするには **、WrapCompressedRTFStream 関数を使用する必要** があります。 
  
## <a name="see-also"></a>関連項目

- [圧縮 RTF でメッセージの本文を取得し、それをネイティブ形式に変換する](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

