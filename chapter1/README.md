# api

string类

size()


```

struct user_profile {
	string       name;
	int          guesses;
	int          correct;
	int          level;

    num_sequence cur_seq;
	pvec         cur_seq_vec;
	int          pos;
};

enum num_sequence { ns_unk,
     ns_fib, ns_pell, ns_lucas, ns_tri, ns_sq, ns_pent,
	 ns_cnt = 6, ns_wrong_msg = 4
};

void reset_seq( user_profile *puser )
{
	static string wherefrom( "reset_seq" );

	int new_seq = gen_seq_id( reinterpret_cast<unsigned int>( puser ));
	if ( new_seq == puser->cur_seq )
		 new_seq = new_seq < ns_cnt ? new_seq+1 : 1;

	puser->cur_seq = static_cast<num_sequence>( new_seq );

	set_up_index( puser );

	print_seq( puser );
	trace( wherefrom, "new sequence: ", name_seq[ puser->cur_seq ]);
}

ch1.cpp: In function ‘void reset_seq(user_profile*)’:
ch1.cpp:253:72: error: cast from ‘user_profile*’ to ‘unsigned int’ loses precision [-fpermissive]

```

