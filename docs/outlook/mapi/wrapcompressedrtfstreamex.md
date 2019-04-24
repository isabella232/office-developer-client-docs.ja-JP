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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325775"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**適用対象**: Outlook 2013 | Outlook 2016 
  
圧縮されたリッチテキスト形式 (RTF) の電子メールメッセージの本文を伸張し、圧縮されていないストリームの形式を示し、必要に応じて圧縮解除したストリームをネイティブ形式に変換して、圧縮解除されたストリームまたはのいずれかを返します。変換されたネイティブストリーム。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |msmapi32  <br/> |
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

_lp圧縮 sedrtfstream_
  
> 順番これは、メッセージの[PidTagRtfCompressed 標準プロパティ](pidtagrtfcompressed-canonical-property.md)で開かれるストリームへのポインターです。 
    
_pWCSInfo_
  
> 順番これは、 
    
   関数のオプションを含む[RTF_WCSINFO](rtf_wcsinfo.md)構造体。 
    
_lpp非圧縮 sedrtfstream_
  
> 読み上げこれは、解凍された RTF のストリームが返される場所へのポインターです。 
    
_この情報_
  
> 読み上げこれは、返された圧縮解除ストリームの形式に関する情報を含む[RTF_WCSRETINFO](rtf_wcsretinfo.md)構造体へのポインターです。 
    
## <a name="return-values"></a>戻り値

S_OK 
  
- 関数呼び出しが成功しました。
    
MAPI_E_INVALID_PARAMETER 
  
- これは、 **MAPI_NATIVE_BODY**フラグが*pWCSInfo*で示される**RTF_WCSINFO**構造の**ulflags**フィールドの**MAPI_MODIFY**フラグと組み合わされている場合に返されます。 
    
## <a name="remarks"></a>解説

**WrapCompressedRTFStreamEx**では、ストリームを解凍することで、圧縮された RTF でカプセル化された電子メールメッセージの本文にアクセスし、圧縮解除されたストリームとその形式、および必要に応じてネイティブ本文ストリームを返します。 ネイティブ本文のストリームは、RTF、プレーンテキスト、または HTML のいずれかにすることができます。 
  
Microsoft Office Outlook オブジェクトモデルには、 **mailitem**オブジェクトの**body**プロパティと、本文テキストの形式を示す[BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)が用意されています。 設計上、outlook によって信頼されていないソリューションは、outlook セキュリティガードによって生成されるセキュリティダイアログボックスを呼び出します。 エクスポートされた mapi 関数**WrapCompressedRTFStreamEx**を使用すると、ソリューションは Outlook オブジェクトモデルではなく mapi を使用し、これらのセキュリティダイアログボックスを回避することができます。 
  
**mapi\_NATIVE_BODY**フラグは、 *pWCSInfo*によって参照されている**\_RTF WCSINFO**構造の**ulflags**フィールドに**mapi\_の変更**フラグと組み合わせて使用することはできないため、ネイティブのみにアクセスできます。読み取り専用モードの本文ストリーム。 読み取り/書き込みモードでネイティブ本文ストリームにアクセスするには、 **WrapCompressedRTFStream**関数を使用する必要があります。 
  
## <a name="see-also"></a>関連項目

- [圧縮 RTF でメッセージの本文を取得し、それをネイティブ形式に変換する](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

