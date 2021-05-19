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
  
プライベート ファイルへのパスを返Mapi32.dll。
  
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
  
> [in]MSIComponentID reg キーは、スタブ レジストリMapi32.dll[で説明](https://msdn.microsoft.com/library/dd162409.aspx)設定。
    
 _szQualifier_
  
> [in]「読み込む MAPI の特定のバージョンを選択する」で説明されている MSIApplicationLCID または MSIOfficeLCID [サブキー](how-to-choose-a-specific-version-of-mapi-to-load.md)。 修飾子がない場合、 **呼** び出し元は null を渡すことができます。 
    
 _szDllPath_
  
> [in]MAPI の完全な機能をMapi32.dllプライベート インターフェイスへのパス (エクスポートと同じ) Mapi32.dll。
    
 _cchBufferSize_
  
> [in]  _szDllPath のサイズ_(文字)。
    
 _fInstall_
  
> [in]プライベート コンポーネントが存在しない場合Mapi32.dll MAPI にインストールを指示します。
    
## <a name="return-value"></a>戻り値

 **true**
  
> パスが見つかりました。
    
 **false**
  
> パスが見つかりませんでした。
    
## <a name="remarks"></a>注釈

プライベート コンポーネントへのパスを取得する必要がある場合は **、FGetComponentPath** 関数を使用Mapi32.dll。 
  
## <a name="see-also"></a>関連項目



[読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dllスタブ レジストリ 設定](https://msdn.microsoft.com/library/dd162409.aspx)

