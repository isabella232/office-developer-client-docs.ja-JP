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
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800045"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**適用対象**: Outlook 
  
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
  
> [in][Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/en-us/library/dd162409.aspx)」で説明する MSIComponentID レジストリ キーです。
    
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
    
## <a name="remarks"></a>注釈

プライベート Mapi32.dll へのパスを取得したい場合に、 **FGetComponentPath**関数を使用します。 
  
## <a name="see-also"></a>関連項目



[読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll スタブのレジストリ設定](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

