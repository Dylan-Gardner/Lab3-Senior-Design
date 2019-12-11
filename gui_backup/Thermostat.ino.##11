//<File !Start!>
// FILE: [Thermostat.ino]
// Created by GUIslice Builder version: [0.13.b009]
//
// GUIslice Builder Generated File
//
// For the latest guides, updates and support view:
// https://github.com/ImpulseAdventure/GUIslice
//
//<File !End!>
//
// ARDUINO NOTES:
// - GUIslice_config.h must be edited to match the pinout connections
//   between the Arduino CPU and the display controller (see ADAGFX_PIN_*).
//

// ------------------------------------------------
// Headers to include
// ------------------------------------------------
#include "GUIslice.h"
#include "GUIslice_drv.h"

// Include any extended elements
//<Includes !Start!>
//<Includes !End!>

// ------------------------------------------------
// Headers and Defines for fonts
// Note that font files are located within the Adafruit-GFX library folder:
// ------------------------------------------------
//<Fonts !Start!>
//<Fonts !End!>

// ------------------------------------------------
// Defines for resources
// ------------------------------------------------
//<Resources !Start!>
//<Resources !End!>

// ------------------------------------------------
// Enumerations for pages, elements, fonts, images
// ------------------------------------------------
//<Enum !Start!>
enum {E_PG_MAIN,E_PG2,E_PG3};
enum {AC_BTN,AUTO_BTN,CUR_TEMP_TEXT,DATE_TEXT,DOWN_BTN,E_DRAW_LINE1
      ,E_ELEM_BTN22,E_ELEM_BTN23,E_ELEM_BTN24,E_ELEM_BTN25,E_ELEM_BTN26
      ,E_ELEM_BTN27,E_ELEM_BTN28,E_ELEM_BTN29,E_ELEM_BTN30,E_ELEM_BTN31
      ,E_ELEM_BTN32,E_ELEM_BTN33,E_ELEM_TEXT10,E_ELEM_TEXT11
      ,E_ELEM_TEXT12,E_ELEM_TEXT13,E_ELEM_TEXT14,E_ELEM_TEXT7
      ,E_ELEM_TEXT8,E_ELEM_TEXT9,HEAT_BTN,HOLD_BTN,HOME_BUTTON_1
      ,HOME_BUTTON_2,OFF_BTN,PRGM_BTN,SETTINGS_BTN,SET_TEMP_TEXT,UP_BNT
      ,WKND_1_BTN,WKND_2_BTN,WKND_3_BTN,WKND_4_BTN,WK_1_BTN,WK_2_BTN
      ,WK_3_BTN,WK_4_BTN};
// Must use separate enum for fonts with MAX_FONT at end to use gslc_FontSet.
enum {E_FONT_TXT5,MAX_FONT};
//<Enum !End!>

// ------------------------------------------------
// Instantiate the GUI
// ------------------------------------------------

// ------------------------------------------------
// Define the maximum number of elements and pages
// ------------------------------------------------
//<ElementDefines !Start!>
#define MAX_PAGE                3

#define MAX_ELEM_PG_MAIN 12 // # Elems total on page
#define MAX_ELEM_PG_MAIN_RAM MAX_ELEM_PG_MAIN // # Elems in RAM

#define MAX_ELEM_PG2 12 // # Elems total on page
#define MAX_ELEM_PG2_RAM MAX_ELEM_PG2 // # Elems in RAM

#define MAX_ELEM_PG3 19 // # Elems total on page
#define MAX_ELEM_PG3_RAM MAX_ELEM_PG3 // # Elems in RAM
//<ElementDefines !End!>

// ------------------------------------------------
// Create element storage
// ------------------------------------------------
gslc_tsGui                      m_gui;
gslc_tsDriver                   m_drv;
gslc_tsFont                     m_asFont[MAX_FONT];
gslc_tsPage                     m_asPage[MAX_PAGE];

//<GUI_Extra_Elements !Start!>
gslc_tsElem                     m_asPage1Elem[MAX_ELEM_PG_MAIN_RAM];
gslc_tsElemRef                  m_asPage1ElemRef[MAX_ELEM_PG_MAIN];
gslc_tsElem                     m_asPage2Elem[MAX_ELEM_PG2_RAM];
gslc_tsElemRef                  m_asPage2ElemRef[MAX_ELEM_PG2];
gslc_tsElem                     m_asPage3Elem[MAX_ELEM_PG3_RAM];
gslc_tsElemRef                  m_asPage3ElemRef[MAX_ELEM_PG3];

#define MAX_STR                 100

//<GUI_Extra_Elements !End!>

// ------------------------------------------------
// Program Globals
// ------------------------------------------------

// Save some element references for direct access
//<Save_References !Start!>
//<Save_References !End!>

// Define debug message function
static int16_t DebugOut(char ch) { if (ch == (char)'\n') Serial.println(""); else Serial.write(ch); return 0; }

// ------------------------------------------------
// Callback Methods
// ------------------------------------------------
// Common Button callback
bool CbBtnCommon(void* pvGui,void *pvElemRef,gslc_teTouch eTouch,int16_t nX,int16_t nY)
{
  gslc_tsElemRef* pElemRef = (gslc_tsElemRef*)(pvElemRef);
  gslc_tsElem* pElem = pElemRef->pElem;

  if ( eTouch == GSLC_TOUCH_UP_IN ) {
    // From the element's ID we can determine which button was pressed.
    switch (pElem->nId) {
//<Button Enums !Start!>

      case DOWN_BTN:
        //TODO- Replace with button handling code
        break;
      case PRGM_BTN:
        //TODO- Check the code to see what else you may need to add
        gslc_SetPageCur(&m_gui,E_PG2);
        break;
      case SETTINGS_BTN:
        //TODO- Replace with button handling code
        break;
      case HOLD_BTN:
        //TODO- Replace with button handling code
        break;
      case HEAT_BTN:
        //TODO- Replace with button handling code
        break;
      case AC_BTN:
        //TODO- Replace with button handling code
        break;
      case AUTO_BTN:
        //TODO- Replace with button handling code
        break;
      case OFF_BTN:
        //TODO- Replace with button handling code
        break;
      case HOME_BUTTON_1:
        //TODO- Check the code to see what else you may need to add
        gslc_SetPageCur(&m_gui,E_PG_MAIN);
        break;
      case WK_1_BTN:
        //TODO- Replace with button handling code
        break;
      case WK_2_BTN:
        //TODO- Replace with button handling code
        break;
      case WK_3_BTN:
        //TODO- Replace with button handling code
        break;
      case WK_4_BTN:
        //TODO- Replace with button handling code
        break;
      case WKND_1_BTN:
        //TODO- Replace with button handling code
        break;
      case WKND_2_BTN:
        //TODO- Replace with button handling code
        break;
      case WKND_3_BTN:
        //TODO- Replace with button handling code
        break;
      case WKND_4_BTN:
        //TODO- Replace with button handling code
        break;
      case HOME_BUTTON_2:
        //TODO- Check the code to see what else you may need to add
        gslc_SetPageCur(&m_gui,E_PG_MAIN);
        break;
      case E_ELEM_BTN22:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN23:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN24:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN25:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN26:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN27:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN28:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN29:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN30:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN31:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN32:
        //TODO- Replace with button handling code
        break;
      case E_ELEM_BTN33:
        //TODO- Replace with button handling code
        break;
      case UP_BNT:
        //TODO- Replace with button handling code
        break;
//<Button Enums !End!>
      default:
        break;
    }
  }
  return true;
}
//<Checkbox Callback !Start!>
//<Checkbox Callback !End!>
//<Keypad Callback !Start!>
//<Keypad Callback !End!>
//<Spinner Callback !Start!>
//<Spinner Callback !End!>
//<Listbox Callback !Start!>
//<Listbox Callback !End!>
//<Draw Callback !Start!>
//<Draw Callback !End!>
//<Slider Callback !Start!>
//<Slider Callback !End!>
//<Tick Callback !Start!>
//<Tick Callback !End!>

// ------------------------------------------------
// Create page elements
// ------------------------------------------------
bool InitGUI()
{
  gslc_tsElemRef* pElemRef = NULL;

//<InitGUI !Start!>
  gslc_PageAdd(&m_gui,E_PG_MAIN,m_asPage1Elem,MAX_ELEM_PG_MAIN_RAM,m_asPage1ElemRef,MAX_ELEM_PG_MAIN);
  gslc_PageAdd(&m_gui,E_PG2,m_asPage2Elem,MAX_ELEM_PG2_RAM,m_asPage2ElemRef,MAX_ELEM_PG2);
  gslc_PageAdd(&m_gui,E_PG3,m_asPage3Elem,MAX_ELEM_PG3_RAM,m_asPage3ElemRef,MAX_ELEM_PG3);

  // NOTE: The current page defaults to the first page added. Here we explicitly
  //       ensure that the main page is the correct page no matter the add order.
  gslc_SetPageCur(&m_gui,E_PG_MAIN);
  
  // Set Background to a flat color
  gslc_SetBkgndColor(&m_gui,GSLC_COL_WHITE);

  // -----------------------------------
  // PAGE: E_PG_MAIN
  
  
  // Create SET_TEMP_TEXT text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,SET_TEMP_TEXT,E_PG_MAIN,(gslc_tsRect){148,110,24,10},
    (char*)"Temp",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_BLACK,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create CUR_TEMP_TEXT text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,CUR_TEMP_TEXT,E_PG_MAIN,(gslc_tsRect){20,110,72,10},
    (char*)"Current Temp",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY_DK3,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create DATE_TEXT text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,DATE_TEXT,E_PG_MAIN,(gslc_tsRect){10,10,24,10},
    (char*)"Date",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // create DOWN_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,DOWN_BTN,E_PG_MAIN,
    (gslc_tsRect){120,140,80,40},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create PRGM_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,PRGM_BTN,E_PG_MAIN,
    (gslc_tsRect){260,10,50,30},(char*)"Program",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create SETTINGS_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,SETTINGS_BTN,E_PG_MAIN,
    (gslc_tsRect){50,10,60,30},(char*)"Settings",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create HOLD_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,HOLD_BTN,E_PG_MAIN,
    (gslc_tsRect){240,100,40,30},(char*)"Hold",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create HEAT_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,HEAT_BTN,E_PG_MAIN,
    (gslc_tsRect){10,190,40,40},(char*)"Heat",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create AC_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,AC_BTN,E_PG_MAIN,
    (gslc_tsRect){70,190,40,40},(char*)"AC",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create AUTO_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,AUTO_BTN,E_PG_MAIN,
    (gslc_tsRect){130,190,40,40},(char*)"Auto",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create OFF_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,OFF_BTN,E_PG_MAIN,
    (gslc_tsRect){190,190,40,40},(char*)"Off",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create UP_BNT button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,UP_BNT,E_PG_MAIN,
    (gslc_tsRect){120,50,80,40},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);

  // -----------------------------------
  // PAGE: E_PG2
  
  
  // create HOME_BUTTON_1 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,HOME_BUTTON_1,E_PG2,
    (gslc_tsRect){150,200,30,30},(char*)"Home",0,E_FONT_TXT5,&CbBtnCommon);
  
  // Create E_ELEM_TEXT7 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT7,E_PG2,(gslc_tsRect){30,10,42,10},
    (char*)"Weekday",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create E_ELEM_TEXT8 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT8,E_PG2,(gslc_tsRect){230,10,42,10},
    (char*)"Weekend",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);

  // Create E_DRAW_LINE1 line 
  pElemRef = gslc_ElemCreateLine(&m_gui,E_DRAW_LINE1,E_PG2,0,22,320,22);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_BLACK,GSLC_COL_BLACK,GSLC_COL_BLACK);
  
  // create WK_1_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WK_1_BTN,E_PG2,
    (gslc_tsRect){10,30,80,30},(char*)"Program 1",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WK_2_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WK_2_BTN,E_PG2,
    (gslc_tsRect){10,70,80,30},(char*)"Program 2",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WK_3_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WK_3_BTN,E_PG2,
    (gslc_tsRect){10,110,80,30},(char*)"Program 3",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WK_4_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WK_4_BTN,E_PG2,
    (gslc_tsRect){10,150,80,30},(char*)"Program 4",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WKND_1_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WKND_1_BTN,E_PG2,
    (gslc_tsRect){230,30,80,30},(char*)"Program 1",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WKND_2_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WKND_2_BTN,E_PG2,
    (gslc_tsRect){230,70,80,30},(char*)"Program 2",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WKND_3_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WKND_3_BTN,E_PG2,
    (gslc_tsRect){230,110,80,30},(char*)"Program 3",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create WKND_4_BTN button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,WKND_4_BTN,E_PG2,
    (gslc_tsRect){230,150,80,30},(char*)"Program 4",0,E_FONT_TXT5,&CbBtnCommon);

  // -----------------------------------
  // PAGE: E_PG3
  
  
  // Create E_ELEM_TEXT9 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT9,E_PG3,(gslc_tsRect){20,120,12,10},
    (char*)"12",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create E_ELEM_TEXT10 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT10,E_PG3,(gslc_tsRect){60,120,12,10},
    (char*)"05",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create E_ELEM_TEXT11 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT11,E_PG3,(gslc_tsRect){90,120,24,10},
    (char*)"2019",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // create HOME_BUTTON_2 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,HOME_BUTTON_2,E_PG3,
    (gslc_tsRect){270,10,40,30},(char*)"Home",0,E_FONT_TXT5,&CbBtnCommon);
  
  // Create E_ELEM_TEXT12 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT12,E_PG3,(gslc_tsRect){200,120,6,10},
    (char*)"2",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create E_ELEM_TEXT13 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT13,E_PG3,(gslc_tsRect){220,120,12,10},
    (char*)"58",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // Create E_ELEM_TEXT14 text label
  pElemRef = gslc_ElemCreateTxt(&m_gui,E_ELEM_TEXT14,E_PG3,(gslc_tsRect){250,120,12,10},
    (char*)"AM",0,E_FONT_TXT5);
  gslc_ElemSetTxtCol(&m_gui,pElemRef,GSLC_COL_BLACK);
  gslc_ElemSetCol(&m_gui,pElemRef,GSLC_COL_GRAY,GSLC_COL_WHITE,GSLC_COL_BLACK);
  
  // create E_ELEM_BTN22 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN22,E_PG3,
    (gslc_tsRect){180,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN23 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN23,E_PG3,
    (gslc_tsRect){210,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN24 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN24,E_PG3,
    (gslc_tsRect){240,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN25 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN25,E_PG3,
    (gslc_tsRect){240,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN26 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN26,E_PG3,
    (gslc_tsRect){210,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN27 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN27,E_PG3,
    (gslc_tsRect){180,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN28 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN28,E_PG3,
    (gslc_tsRect){10,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN29 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN29,E_PG3,
    (gslc_tsRect){10,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN30 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN30,E_PG3,
    (gslc_tsRect){50,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN31 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN31,E_PG3,
    (gslc_tsRect){90,140,30,30},(char*)"Down",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN32 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN32,E_PG3,
    (gslc_tsRect){50,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
  
  // create E_ELEM_BTN33 button with text label
  pElemRef = gslc_ElemCreateBtnTxt(&m_gui,E_ELEM_BTN33,E_PG3,
    (gslc_tsRect){90,70,30,30},(char*)"Up",0,E_FONT_TXT5,&CbBtnCommon);
//<InitGUI !End!>

  return true;
}

void setup()
{
  // ------------------------------------------------
  // Initialize
  // ------------------------------------------------
  Serial.begin(9600);
  // Wait for USB Serial 
  //delay(1000);  // NOTE: Some devices require a delay after Serial.begin() before serial port can be used

  gslc_InitDebug(&DebugOut);

  if (!gslc_Init(&m_gui,&m_drv,m_asPage,MAX_PAGE,m_asFont,MAX_FONT)) { return; }

  // ------------------------------------------------
  // Load Fonts
  // ------------------------------------------------
//<Load_Fonts !Start!>
    if (!gslc_FontSet(&m_gui,E_FONT_TXT5,GSLC_FONTREF_PTR,NULL,1)) { return; }
//<Load_Fonts !End!>

  // ------------------------------------------------
  // Create graphic elements
  // ------------------------------------------------
  InitGUI();

//<Startup !Start!>
  gslc_GuiRotate(&m_gui, 1);
//<Startup !End!>

}

// -----------------------------------
// Main event loop
// -----------------------------------
void loop()
{

  // ------------------------------------------------
  // Update GUI Elements
  // ------------------------------------------------
  
  //TODO - Add update code for any text, gauges, or sliders
  
  // ------------------------------------------------
  // Periodically call GUIslice update function
  // ------------------------------------------------
  gslc_Update(&m_gui);
    
}

