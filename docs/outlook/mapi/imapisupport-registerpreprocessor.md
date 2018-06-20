---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800789"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。 
  
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

## <a name="parameters"></a>Parameters

 _lpMuid_
  
> [in]プリプロセッサ関数を処理するための識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 _LpMuid_パラメーターは NULL にできます。 
    
 _lpszAdrType_
  
> [in]メッセージのアドレスの種類へのポインター、関数では、FAX、SMTP、または X500 などです。 _LpszAdrType_パラメーターは NULL にできます。 
    
 _lpszDLLName_
  
> [in]プリプロセッサ関数のエントリ ポイントを含むダイナミック リンク ライブラリ (DLL) の名前へのポインター。
    
 _lpszPreprocess_
  
> [in]プリプロセッサ関数の名前へのポインター。 _LpszPreprocess_パラメーターは NULL にできます。 
    
 _lpszRemovePreprocessInfo_
  
> [in]プリプロセッサの情報 ( [RemovePreprocessInfo](removepreprocessinfo.md)のプロトタイプに準拠する関数) を削除する関数の名前へのポインター。 _LpszRemovePreprocessInfo_パラメーターは NULL にできます。 
    
 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プリプロセッサ関数が正常に登録されました。
    
## <a name="remarks"></a>備考

だけに、トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::RegisterPreprocessor**メソッドを実装します。 トランスポート プロバイダーは、プリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録するのには**RegisterPreprocessor**を呼び出します。 MAPI スプーラーを呼び出すことができますには、プリプロセッサ関数を登録する必要があります。 
  
_LpszPreprocess_、 _lpszRemovePreprocessInfo_、および_lpszDLLName_パラメーター、Win32 の**GetProcAddress**関数をプリプロセッサの DLL への呼び出しと組み合わせて使用できる文字列を参照する必要があります。正しく呼び出されるエントリ ポイントです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プリプロセッサの呼び出しでは、トランスポート プロバイダーの順序に固有です。 これは、する場合は、プロバイダーの前に別のトランスポート プロバイダーは、メッセージを処理することが、プリプロセッサ関数は呼び出されませんそのメッセージを意味します。 プリプロセッサ関数は、処理するメッセージに対してのみ呼び出されます。
  
[MAPIUID](mapiuid.md)構造体、またはアドレスの種類に格納されているか、特定 id を処理するためのプリプロセッサ関数を記述できます。 _LpMuid_パラメーターおよび_lpszAdrType_パラメーターのアドレスの種類で、両方の**MAPIUID**構造体を指定すると、 **MAPIUID**またはアドレスの種類のいずれかに一致するメッセージの受信者に対して、関数が呼び出されます。 _LpMuid_は、NULL、 _lpszAdrType_は、NULL 以外の場合は、 _lpszAdrType_で指定された型に一致するアドレスを持つ受信者にのみ、関数が呼び出されます。 _LpMuid_は、NULL ではないし、 _lpszAdrType_が NULL の場合、受信者のアドレスの種類に関係なく**MAPIUID**に一致するため、関数が呼び出されます。 両方が NULL である場合、メッセージのすべての受信者に対して、関数が呼び出されます。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

