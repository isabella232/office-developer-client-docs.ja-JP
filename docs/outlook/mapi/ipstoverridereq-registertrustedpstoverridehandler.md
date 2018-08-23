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
description: '最終更新日: 2013 年 2 月 24 日'
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801186"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**適用対象**: Outlook 
  
個人用フォルダー (.pst) ファイルのロックを解除する手順を開始します。
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>パラメーター

 _pwzDllPath_
  
> [in]サード ・ パーティ製のダイナミック リンク ライブラリ (DLL) のパスへのポインター。
    
 _pvClientData_
  
> [in]PST プロバイダーが DLL の HrTrustedPSTOverrideHandlerCallback 関数への後続の呼び出しに渡されます、クライアントのデータへのポインター。 DLL によっては、このクライアント データを pst ファイルのロックが解除する必要があるかどうかを確認するために使用できます。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 関数の呼び出しに成功しました。
    
## <a name="remarks"></a>注釈

WzDllPath パラメーターで指定された DLL は、デジタル証明書を使用して署名する必要があります。 DLL では、次のシグネチャを持つ関数をエクスポートする必要がありますもします。
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Pst ファイルの IMsgStore オブジェクトへのポインター、IPSTOVERRIDE1 インターフェイスを実装する IUnknown オブジェクトへのポインター、および pvClientData を最初に入力したデータへのポインターでは、この関数が呼び出されます。
  
詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](http://support.microsoft.com/kb/956070)を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

