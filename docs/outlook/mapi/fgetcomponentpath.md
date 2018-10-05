---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384501"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プライベート Mapi32.dll へのパスを返します。
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>パラメーター

 _szComponent_
  
> [in][Mapi32.dll スタブのレジストリ設定](https://msdn.microsoft.com/library/dd162409.aspx)」で説明する MSIComponentID レジストリ キーです。
    
 _szQualifier_
  
> [in]MSIApplicationLCID または MSIOfficeLCID のサブキーを[特定のバージョンの MAPI 負荷を選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)」に記載します。 修飾子がない場合、呼び出し元が**null**渡すことができます。 
    
 _szDllPath_
  
> [in]プライベートの Mapi32.dll は、すべての MAPI 機能 (、Mapi32.dll と同じエクスポート) を持つへのパス。
    
 _cchBufferSize_
  
> [in]_SzDllPath_、文字のサイズです。
    
 _fInstall_
  
> [in]それが存在しない場合は、プライベート、Mapi32.dll コンポーネントをインストールするのには MAPI を指示します。
    
## <a name="return-value"></a>戻り値

 **true**
  
> パスが見つかりました。
    
 **false**
  
> パスが見つかりませんでした。
    
## <a name="remarks"></a>備考

プライベート Mapi32.dll へのパスを取得したい場合に、 **FGetComponentPath**関数を使用します。 
  
## <a name="see-also"></a>関連項目



[読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll スタブのレジストリ設定](https://msdn.microsoft.com/library/dd162409.aspx)

