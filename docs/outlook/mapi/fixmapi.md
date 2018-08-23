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
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800058"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**適用対象**: Outlook 
  
によってバックアップ コピーが mapi32.dll のコピーの現在のクライアント コンピューター、および MAPI スタブ ライブラリのリストア mapi32.dll mapistub.dll。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |mapistub.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>戻り値

関数が成功した場合は、0 以外の値を返します。
  
関数が失敗した場合は 0 を返します。 拡張エラー情報を取得するには、Microsoft Windows ソフトウェア開発キット (SDK) 関数、 **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)** を呼び出します。 
  
## <a name="remarks"></a>注釈

 **FixMAPI**では、ファイルが読み取り専用としてマークされている場合、現在の mapi32.dll ファイルは置換されません。 
  
 **FixMAPI**では、Microsoft Exchange Server がコンピューターにインストールされている場合、現在の mapi32.dll は置換されません。 
  
**FixMAPI**では、特定のコンピューター上の mapi32.dll のコピーの現在のバックアップ ・ コピーと [mapi32.dll] から別の名前がバックアップ ・ コピーで割り当てられます。 バックアップ ・ コピーには、そのアセンブリの後続の呼び出しを指示します。 
  
## <a name="see-also"></a>関連項目



[KB 256946: Outlook 2000 を起動したときにプログラムの競合のエラー メッセージが表示されます。](http://support.microsoft.com/kb/256946)
  
[KB 228457: Fixmapi.exe ツールの説明は、Internet Explorer 5 に含まれる](http://support.microsoft.com/kb/228457)

