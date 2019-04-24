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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335211"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プライベート Mapi32 へのパスを返します。
  
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

 _szcomponent_
  
> 順番[Mapi32 スタブレジストリ設定](https://msdn.microsoft.com/library/dd162409.aspx)に記述されている MSIComponentID reg キー。
    
 _szqualifier_
  
> 順番「[読み込む特定のバージョンの MAPI を選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)」で説明されている msiapplicationlcid または msiofficeelcid サブキー。 修飾子がない場合、発信者は**null**を渡すことができます。 
    
 _szdllpath_
  
> 順番完全な MAPI 機能 (Mapi32 と同じエクスポート) を持つ、プライベート Mapi32 へのパスです。
    
 _cchbuffersize_
  
> 順番_szdllpath_のサイズ (文字数)。
    
 _finstall_
  
> 順番プライベートの Mapi32 コンポーネントが存在しない場合は、そのコンポーネントをインストールするように MAPI に指示します。
    
## <a name="return-value"></a>戻り値

 **false**
  
> パスが見つかりました。
    
 **false**
  
> パスが見つかりませんでした。
    
## <a name="remarks"></a>解説

**FGetComponentPath**関数は、プライベート Mapi32 へのパスを取得する必要がある場合に使用します。 
  
## <a name="see-also"></a>関連項目



[読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32 スタブのレジストリ設定](https://msdn.microsoft.com/library/dd162409.aspx)

