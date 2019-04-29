---
title: imapisupportregisterpreprocessor プロセッサ
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404898"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。 
  
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

 _lpmuid_
  
> 順番プリプロセッサ関数が処理する識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 _lpmuid_パラメーターは NULL にすることができます。 
    
 _lpszadrtype_
  
> 順番FAX、SMTP、または X500 など、関数が操作するメッセージのアドレスの種類へのポインター。 _lpszadrtype_パラメーターは NULL にすることができます。 
    
 _lpszDLLName_
  
> 順番プリプロセッサ関数のエントリポイントが格納されているダイナミックリンクライブラリ (DLL) の名前へのポインター。
    
 _lpszpreprocess_
  
> 順番プリプロセッサ関数の名前へのポインター。 _lpszpreprocess_パラメーターは NULL にすることができます。 
    
 _lpszremovepreprocessinfo_
  
> 順番プリプロセッサ情報 ( [removepreprocessinfo](removepreprocessinfo.md)プロトタイプに準拠する関数) を削除する関数の名前へのポインター。 _lpszremovepreprocessinfo_パラメーターは NULL にすることができます。 
    
 _ulFlags_
  
> 予約語0である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プリプロセッサ関数が正常に登録されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: registerpreprocessor プロセッサ**メソッドは、トランスポートプロバイダーサポートオブジェクトのみに実装されています。 トランスポートプロバイダーは、 **registerpreprocessor**プロセッサを呼び出してプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。 MAPI スプーラーが呼び出す前に、プリプロセッサ関数を登録する必要があります。 
  
_lpszpreprocess_、 _lpszremovepreprocessinfo_、および_lpszDLLName_パラメーターは、Win32 **GetProcAddress**関数への呼び出しと共に使用できる文字列をポイントする必要があります。これにより、プリプロセッサの DLL を使用できるようになります。エントリポイントが正しく呼び出されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

preprocessors の呼び出しは、トランスポートプロバイダーの順序によって異なります。 これは、プロバイダーよりも前の別のトランスポートプロバイダーがメッセージを処理できる場合、そのメッセージに対してプリプロセッサ関数が呼び出されないことを意味します。 プリプロセッサ関数は、処理するメッセージに対してのみ呼び出されます。
  
プリプロセッサ関数を記述して、 [MAPIUID](mapiuid.md)構造またはアドレスの種類に格納されている特定の識別子を処理することができます。 _lpmuid_パラメーターに**MAPIUID**構造体と、 _lpszadrtype_パラメーターにアドレスの種類の両方を指定すると、 **MAPIUID**またはアドレスの種類のいずれかに一致するメッセージ受信者に対して、関数が呼び出されます。 _lpmuid_が null で、 _lpszadrtype_が null 以外の場合、この関数は、 _lpszadrtype_で指定された型に一致するアドレスを持つ受信者に対してのみ呼び出されます。 _lpmuid_が null 以外で、 _lpszadrtype_が null の場合、アドレスの種類に関係なく、 **MAPIUID**に一致する受信者に対して関数が呼び出されます。 両方の値が NULL の場合は、メッセージのすべての受信者に対して関数が呼び出されます。
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

