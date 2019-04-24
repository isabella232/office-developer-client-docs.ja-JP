---
title: MAPI クラッシュ回復 API を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346425"
---
# <a name="use-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API を使用する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックには、C++ のコードサンプルが含まれています。このコードは、[アン handledexceptionfilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx)関数から[mapicrashrecovery](mapicrashrecovery.md)関数を呼び出す方法を示しています。 [mapicrashrecovery](mapicrashrecovery.md)関数は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックします。 

メモリが一貫した状態にある場合、 [mapicrashrecovery](mapicrashrecovery.md)関数はデータをディスクに移動し、プロセスが終了するまで追加の読み取りまたは書き込みアクセスを禁止します。 プロセスが終了する前に、pst または ost が一貫した状態になっていることを確認することにより、microsoft outlook 2010 または microsoft outlook 2013 が次のエラーメッセージを表示しないようにして、パフォーマンスの問題を回避することができます。 
  
**データファイルが前回使用され、問題がないかチェックされているときに、データファイルが正常に閉じられませんでした。チェックが進行している間は、パフォーマンスが影響を受ける可能性があります。**
  
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

