---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: '最終更新日: 2013 年 2 月 24 日'
ms.openlocfilehash: c7c074bbfb365d8a975bee12c5611c4d0809dc1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620535"
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
  
> [in]サードパーティのダイナミック リンク ライブラリ (DLL) のパスへのポインター。
    
 _pvClientData_
  
> [in]クライアント データへのポインター。これは、PST プロバイダーによって DLL の HrTrustedPSTOverrideHandlerCallback 関数への後続の呼び出しに渡されます。 このクライアント データは、PST をロック解除する必要があるかどうかを確認するために DLL で使用できます。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

wzDllPath パラメーターで指定された DLL は、デジタル証明書を使用して署名する必要があります。 DLL は、次のシグネチャを持つ関数もエクスポートする必要があります。
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

この関数は、PST の IMsgStore オブジェクトへのポインター、IPSTOVERRIDE1 インターフェイスを実装する IUnknown オブジェクトへのポインター、および pvClientData を介して最初に提供されたデータへのポインターを使用して呼び出されます。
  
詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

