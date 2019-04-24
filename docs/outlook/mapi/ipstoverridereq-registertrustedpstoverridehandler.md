---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: '最終更新日: 2013 年2月24日'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279536"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー (.pst) ファイルのロック解除手順を開始します。
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>パラメーター

 _pwzDllPath_
  
> 順番サードパーティのダイナミックリンクライブラリ (DLL) のパスへのポインター。
    
 _pvclientdata_
  
> 順番クライアントデータへのポインター。 PST プロバイダによって、その後の DLL の HrTrustedPSTOverrideHandlerCallback 関数への呼び出しに渡されます。 このクライアントデータは、PST のロックを解除する必要があるかどうかの確認を支援するために DLL によって使用されます。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>解説

wzDllPath パラメーターで指定された DLL は、デジタル証明書を使用して署名する必要があります。 DLL は、次のシグネチャを持つ関数もエクスポートする必要があります。
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

この関数は、PST の IMsgStore オブジェクトへのポインター、IPSTOVERRIDE1 インターフェイスを実装する IUnknown オブジェクトへのポインター、および pvclientdata から最初に提供されたデータへのポインターを使用して呼び出されます。
  
詳細については、「 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするように PST オーバーライドハンドラーを実装する方法](https://support.microsoft.com/kb/956070)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

