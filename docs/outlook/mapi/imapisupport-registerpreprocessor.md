---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2d427dbf998a04f36e384baa7f029baa755b5d73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556505"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーのプリプロセッサ関数 [(PreprocessMessage](preprocessmessage.md) プロトタイプに準拠する関数) を登録します。 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMuid_
  
> [in]プリプロセッサ関数が処理する識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 _lpMuid パラメーター_ には NULL を指定できます。 
    
 _lpszAdrType_
  
> [in]FAX、SMTP、X500 など、関数が操作するメッセージのアドレスの種類へのポインター。 _lpszAdrType パラメーター_ には NULL を指定できます。 
    
 _lpszDLLName_
  
> [in]プリプロセッサ関数のエントリ ポイントを含むダイナミック リンク ライブラリ (DLL) の名前へのポインター。
    
 _lpszPreprocess_
  
> [in]プリプロセッサ関数の名前へのポインター。 _lpszPreprocess パラメーター_ には NULL を指定できます。 
    
 _lpszRemovePreprocessInfo_
  
> [in]プリプロセッサ情報 [(RemovePreprocessInfo](removepreprocessinfo.md) プロトタイプに準拠する関数) を削除する関数の名前へのポインター。 _lpszRemovePreprocessInfo_ パラメーターには NULL を指定できます。 
    
 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プリプロセッサ関数が正常に登録されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::RegisterPreprocessor メソッド** は、トランスポート プロバイダーのサポート オブジェクトにのみ実装されます。 トランスポート プロバイダーは **RegisterPreprocessor** を呼び出して、プリプロセッサ関数 [(PreprocessMessage](preprocessmessage.md) プロトタイプに準拠する関数) を登録します。 MAPI スプーラーが呼び出す前に、プリプロセッサ関数を登録する必要があります。 
  
_lpszPreprocess_ _、lpszRemovePreprocessInfo、__および lpszDLLName_ パラメーターは、すべて Win32 **GetProcAddress** 関数の呼び出しと組み合わせて使用できる文字列を指し示す必要があります。プリプロセッサの DLL エントリ ポイントを正しく呼び出す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プリプロセッサへの呼び出しは、トランスポート プロバイダーの順序に固有です。 つまり、プロバイダーの前に別のトランスポート プロバイダーがメッセージを処理できる場合、そのメッセージに対してプリプロセッサ関数は呼び出されません。 プリプロセッサ関数は、処理するメッセージに対してのみ呼び出されます。
  
[MAPIUID](mapiuid.md)構造体に格納されている特定の識別子またはアドレスの種類を処理するプリプロセッサ関数を記述できます。 _lpMuid_ パラメーターに **MAPIUID** 構造と _lpszAdrType_ パラメーターのアドレス型の両方を指定すると **、MAPIUID** またはアドレスの種類に一致するメッセージ受信者に対して関数が呼び出されます。 _lpMuid が_ NULL で _、lpszAdrType_ が NULL 以外の場合 _、lpszAdrType_ が指す型に一致するアドレスを持つ受信者に対してだけ関数が呼び出されます。 _lpMuid が_ NULL 以外で _lpszAdrType_ が NULL の場合、アドレスの種類に関係なく **、MAPIUID** に一致する受信者に対して関数が呼び出されます。 両方が NULL の場合、メッセージのすべての受信者に対して関数が呼び出されます。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

