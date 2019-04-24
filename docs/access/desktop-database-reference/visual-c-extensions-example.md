---
title: Visual C++ Extensions の例
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 080281ae0deb25fa10fcdccd8577d3aab076c2cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312069"
---
# <a name="visual-c-extensions-example"></a><span data-ttu-id="0c53e-102">Visual C++ Extensions の例</span><span class="sxs-lookup"><span data-stu-id="0c53e-102">Visual C++ Extensions example</span></span>


<span data-ttu-id="0c53e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c53e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c53e-104">このプログラムは、値がフィールドからどのように取得され、C/C++ 変数に変換されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="0c53e-104">This program shows how values are retrieved from fields and converted to C/C++ variables.</span></span>

<span data-ttu-id="0c53e-105">この例では、 **IADORecordBinding**インターフェイスの呼び出しおよび参照カウントに関する COM 固有の詳細を自動的に処理する "スマートポインター" も利用します。</span><span class="sxs-lookup"><span data-stu-id="0c53e-105">This example also takes advantage of "smart pointers," which automatically handle the COM-specific details of calling and reference counting for the **IADORecordBinding** interface.</span></span>

<span data-ttu-id="0c53e-106">スマート ポインターを使用しない場合は、次のようにコーディングします。</span><span class="sxs-lookup"><span data-stu-id="0c53e-106">Without smart pointers, you would code:</span></span>

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

<span data-ttu-id="0c53e-107">スマートポインターを使用すると、次のステートメントを使用して、IADORecordBinding インターフェイスの型から IADORecordBindingPtr 型を派生させることができます。</span><span class="sxs-lookup"><span data-stu-id="0c53e-107">With smart pointers, you derive the IADORecordBindingPtr type from the type from the IADORecordBinding interface with this statement:</span></span>

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

<span data-ttu-id="0c53e-108">そして、次のようにポインターのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0c53e-108">And instantiate the pointer like this:</span></span>

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

<span data-ttu-id="0c53e-109">Visual C++ 拡張機能は**Recordset**オブジェクトによって実装されるので、スマートポインターの "ピクチャ" という\_コンストラクターは、RecordsetPtr ポインター pRs を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="0c53e-109">Because the Visual C++ Extensions are implemented by the **Recordset** object, the constructor for the smart pointer, picRs , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="0c53e-110">コンストラクタは、pRs を使用して QueryInterface を検索し\_、RecordsetPtr ポインター pRs を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c53e-110">The constructor calls QueryInterface using pRs to find the , takes the \_RecordsetPtr pointer, pRs .</span></span> <span data-ttu-id="0c53e-111">コンストラクターは、pRs を使用して QueryInterface を呼び出し、IADORecordBinding インターフェイスを検索します。</span><span class="sxs-lookup"><span data-stu-id="0c53e-111">The constructor calls QueryInterface using pRs to find the IADORecordBinding interface.</span></span>

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

