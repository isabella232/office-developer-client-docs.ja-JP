---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334962"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントコンピューターに mapi32 の現在のコピーのバックアップコピーを作成し、mapi32 を MAPI スタブライブラリ mapistub に復元して復元します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |mapistub  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>戻り値

関数が正常に終了した場合、戻り値は0以外の値になります。
  
関数が失敗した場合、戻り値は0になります。 拡張エラー情報を取得するには、Microsoft Windows Software Development Kit (SDK) 関数 ( **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**) を呼び出します。 
  
## <a name="remarks"></a>解説

 **FixMAPI**は、ファイルが読み取り専用としてマークされている場合は、現在の mapi32 ファイルを置き換えません。 
  
 **FixMAPI**は、Microsoft Exchange Server がコンピューターにインストールされている場合は、現在の mapi32 を置き換えません。 
  
**FixMAPI**がコンピューターに mapi32 の現在のコピーのバックアップコピーを作成すると、"mapi32" とは異なる名前がバックアップコピーに割り当てられます。 その後、そのアセンブリに対する後続の呼び出しがバックアップコピーに送られます。 
  
## <a name="see-also"></a>関連項目



[KB 256946: Outlook 2000 の起動時にプログラムの競合エラーメッセージが表示される](https://support.microsoft.com/kb/256946)
  
[KB 228457: Internet Explorer 5 に含まれる Fixmapi ツールについて説明します。](https://support.microsoft.com/kb/228457)

