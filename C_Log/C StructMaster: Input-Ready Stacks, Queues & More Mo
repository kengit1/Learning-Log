/*
// Helper: Enqueue all characters in a string
void enqueueString(Queue *q, const char *str) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (isFull(q)) break;
        enqueue(q, str[i]);
    }
}
*/ //? a possible improve : improve readability and modularity
Queue * constrctr()
{
    Queue * q_op = init() ;
    /*if (userQueue == NULL) {
        fprintf(stderr, "Failed to initialize queue.\n");
        return NULL;
    }*/ //? a possible check
    char input[MAXSIZE] ;
    printf("Enter your desired form of data...Max is %d for the %s[Type '`' then 'Enter' to finish the inputs]:\n" ,MAXSIZE,dataStruct) ;
    while (!isFull(q_op))
    {
        fgets(input , MAXSIZE , stdin) ;
        /*  if (fgets(input, MAXSIZE, stdin) == NULL) {
            // Handle EOF/error (e.g., Ctrl+D/Ctrl+Z)
            printf("\nInput terminated early.\n");
            break;
        }*/ //? a possible check
        //check your condition
        if(strchr(input , '`'))
        {
            //* removing any possible break to the inputs
            input[strcspn(input, "\n")] = '\0';
            input[strcspn(input, "`")] = '\0';
            //implement into the data strcut.
            for(int i = 0 ; i< strlen(input) ; i++ )
            {
                if(isFull(q_op)) {printf("->The %s is now full!!\n",dataStruct); break;}
                //* ensured that no possible hinders for completion of implementation
                enqueue(q_op , input[i]) ;
            }
            break; //ended the implementation after the '`'
        }
        else
        {
            //* removing any possible break to the inputs and better UI/UX
            input[strcspn(input, "\n")] = '\0';
            input[strcspn(input, "`")] = '\0';
            //implement into the data strcut.
            for(int i = 0 ; i< strlen(input) ; i++ )
            {
                if(isFull(q_op)) {printf("->The %s is now full!!\nAnd without the ending condition i see...\n:(\n",dataStruct); break;}
                //* ensured that no possible hinders for completion of implementation
                enqueue(q_op , input[i]) ;
            }
        }
        //Ending of implementing into the data struct.
    }
    return q_op ;
}
