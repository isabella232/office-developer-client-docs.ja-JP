---
title: 説明、HelpContext、HelpFile プロパティの例 (VC++)
TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VC++)
ms:assetid: 1375a0e6-c61b-aba5-4d7c-5db597ef873e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248908(v=office.15)
ms:contentKeyID: 48543369
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 22481092701482fbed3103ef82340d2d4bbfd1f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553110"
---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vc"></a>Description プロパティ、HelpContext プロパティ、HelpFile プロパティ、NativeError プロパティ、Number プロパティ、Source プロパティ、SQLState プロパティの使用例 (VC++)


**適用先:** Access 2013、Office 2013

この例では、エラーを発生させてトラップし、生成された [Error](description-property-ado.md) オブジェクトの [Description](helpcontext-helpfile-properties-ado.md)、[HelpContext](helpcontext-helpfile-properties-ado.md)、[HelpFile](nativeerror-property-ado.md)、[NativeError](number-property-ado.md)、[Number](source-property-ado-error.md)、[Source](sqlstate-property-ado.md)、および [SQLState](error-object-ado.md) プロパティを表示します。

```cpp
    // BeginDescriptionCpp
    #import "C:\Program Files\Common Files\System\ADO\msado15.dll"     no_namespace rename("EOF", "EndOfFile")
    
    #include <ole2.h>
    #include <stdio.h>
    #include<conio.h>
    
    // Function declarations
    inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);};
    void DescriptionX(void);
    void PrintProviderError(_ConnectionPtr pConnection);
    void PrintComError(_com_error &e);
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      Main Function                                    //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void main()
    {
        if(FAILED(::CoInitialize(NULL)))
            return;
    
        DescriptionX();
    
        //Wait here for user to see the output..
        printf("\nPress any key to continue...");
        getch();
        ::CoUninitialize();
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      DescriptionX Function                            //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void DescriptionX()
    {
        // Define ADO object pointers.
        // Initialize pointers on define.
        // These are in the ADODB::  namespace
        _ConnectionPtr pConnection = NULL;
        ErrorPtr errorLoop = NULL;
    
        //Define Other Variables
        HRESULT hr = S_OK;
        
    
        try
        {
            // Intentionally trigger an error.
            // open connection
            TESTHR(pConnection.CreateInstance(__uuidof(Connection)));
    
            if (FAILED(hr = pConnection->Open("nothing","","",adConnectUnspecified)))
            {
                _com_issue_error(hr);
                exit(1);
            }
    
            // Cleanup object before exit.
            pConnection->Close();
        }
        catch(_com_error)
        {
            // Pass a connection pointer.
            PrintProviderError(pConnection);
        }
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      PrintProviderError Function                      //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void PrintProviderError(_ConnectionPtr pConnection)
    {
        //Define Other Variables
        HRESULT  hr = S_OK;
        _bstr_t  strError;
        ErrorPtr  pErr = NULL;
    
        try
        {
            // Enumerate Errors collection and display
            // properties of each Error object.
            long nCount = pConnection->Errors->Count;
    
            // Collection ranges from 0 to nCount - 1.
            for(long i = 0; i < nCount; i++)
            {
                pErr = pConnection->Errors->GetItem(i);
                printf("Error #%d\n", pErr->Number);
                printf(" %s\n",(LPCSTR)pErr->Description);
                printf(" (Source: %s)\n",(LPCSTR)pErr->Source);
                printf(" (SQL State: %s)\n",(LPCSTR)pErr->SQLState);
                printf(" (NativeError: %d)\n",(LPCSTR)pErr->NativeError);
                if ((LPCSTR)pErr->GetHelpFile() == NULL)
                {
                    printf("\tNo Help file available\n");
                }
                else
                {
                    printf("\t(HelpFile: %s\n)" ,pErr->HelpFile);
                    printf("\t(HelpContext: %s\n)" , pErr->HelpContext);
                }
            }
        }
        catch(_com_error &e)
        {
            // Notify the user of errors if any.
            PrintComError(e);
        }
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      PrintComError Function                           //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void PrintComError(_com_error &e)
    {
       // Notify the user of errors if any.
       _bstr_t bstrSource(e.Source());
       _bstr_t bstrDescription(e.Description());
        
        // Print Com errors.
        
       printf("Error\n");
       printf("\tCode = %08lx\n", e.Error());
       printf("\tCode meaning = %s", e.ErrorMessage());
       printf("\tSource = %s\n", (LPCSTR) bstrSource);
       printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
    }
    // EndDescriptionCpp
```
