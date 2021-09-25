---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d40c06b5bd7e2d2523fb81b702c513c6521518e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621095"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント コンピューター上の現在のコピーのmapi32.dllコピーを作成し、MAPI スタブ ライブラリを使用mapi32.dllを復元します。mapistub.dll。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |mapistub.dll  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>戻り値

関数が成功した場合、戻り値は 0 以外の値になります。
  
関数が失敗した場合、戻り値は 0 です。 拡張エラー情報を取得するには、Microsoft Windows ソフトウェア開発キット (SDK) 関数 **[GetLastError を呼び出します](https://msdn.microsoft.com/library/ms679360.aspx)**。 
  
## <a name="remarks"></a>注釈

 **ファイルが読み** 取り専用としてマークされている場合、FixMAPI は現在mapi32.dllファイルを置き換える必要があります。 
  
 **FixMAPI** は、コンピューターにインストールされているmapi32.dll現在Microsoft Exchange Server置き換えるわけではありません。 
  
**FixMAPI** がコンピューター上の mapi32.dll の現在のコピーのバックアップ コピーを作成すると、バックアップ コピーに "mapi32.dll" とは異なる名前が割り当mapi32.dll。 その後、そのアセンブリを対象とした後続の呼び出しをバックアップ コピーに指示します。 
  
## <a name="see-also"></a>関連項目



[KB 256946: 2000 年から開始すると、プログラムの競合エラー Outlookされます。](https://support.microsoft.com/kb/256946)
  
[KB 228457: 5 に付属Fixmapi.exeツールのInternet Explorer説明](https://support.microsoft.com/kb/228457)

