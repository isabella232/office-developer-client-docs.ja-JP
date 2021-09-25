---
title: MAPI クラッシュ回復 API を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 5398e11320c110e48930f60efb6dc513349d575a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561678"
---
# <a name="use-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API を使用する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは[、UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx)関数から[MAPICrashRecovery](mapicrashrecovery.md)関数を呼び出す方法を示す C++ のコード サンプルを示します。 [MAPICrashRecovery 関数は](mapicrashrecovery.md)、個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) 共有メモリの状態をチェックします。 

メモリが一貫性のある状態にある場合 [、MAPICrashRecovery](mapicrashrecovery.md) 関数はデータをディスクに移動し、プロセスが終了するまで読み取りまたは書き込みアクセスを防止します。 プロセスが終了する前に PST または OST が一貫性のある状態に保たれた場合、Microsoft Outlook 2010 または Microsoft Outlook 2013 が次のエラー メッセージを表示しないようにし、パフォーマンスの問題を回避できます。 
  
**前回使用したデータ ファイルが正しく閉じなかったので、問題がチェックされています。チェックの進行中にパフォーマンスが影響を受ける可能性があります。**
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a>関連項目

- [MAPI クラッシュ回復 API について](about-the-mapi-crash-recovery-api.md) 
- [MAPICrashRecovery](mapicrashrecovery.md)

