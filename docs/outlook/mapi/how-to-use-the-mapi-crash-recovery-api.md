---
title: MAPI クラッシュ回復 API を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 8ac75bfb686496c151b5edc3a692c99a6e47ee96
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800264"
---
# <a name="use-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API を使用する

**適用対象**: Outlook 
  
このトピックには、 [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx)関数から、 [MAPICrashRecovery](mapicrashrecovery.md)関数を呼び出す方法を示す C++ でのコード サンプルが含まれています。 [MAPICrashRecovery](mapicrashrecovery.md)関数は、共有メモリを個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態をチェックします。 

メモリは、一貫性のある状態では、 [MAPICrashRecovery](mapicrashrecovery.md)関数はデータをディスクに移動して、プロセスが終了するまでに、さらに読み取りまたは書き込みアクセスを防ぐことが。 ことによって、pst ファイルまたは Ost 整合性の取れた状態でプロセスが終了する前に、Microsoft Outlook 2010 または Microsoft Outlook 2013 が次のエラー メッセージを表示しないようにして、パフォーマンスの問題を回避できます。 
  
**データ ファイルを閉じませんでした正しく問題の最後に使用されていた、チェックされていること。チェックの実行中に、パフォーマンスは影響を受ける可能性があります。**
  
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

